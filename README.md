# Assignment-1.3-Permute-

public class Main{
    static void permute(int[] A, int[] P, int n){
        for(int i = 0; i < n; i++){
            int next = i;

            while(P[next] >= 0){
                swap(A, i, P[next]);
                int temp = P[next];

                P[next] -= n;
                next = temp;
            }
        }
    }

    static int[] swap(int[] arr, int i, int j){
        int temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
        return arr;
    }

    public static void main(String[] args) {
        int A[] = {1,2,3};
        int P[] = { 4,5,6};
        int n = A.length;

        permute(A, P, n);

        for(int i = 0; i < n; i++)
            System.out.println(A[i]+ " ");
    }
}c
