# Square_matrix
You are given a 2D array of integers ‘A’ of length ’N’x’M’, where ‘N’ is the number of rows and ‘M’ is the number of columns. Check if the given array forms a square matrix and returns its diagonal elements.  A Square matrix is one that has an equal number of rows and columns.
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        int[][] a = {{1}};
        int n=a.length;
        int m =a[0].length;
        int diag[]=new int[n];
        String sk=sqrMat(a,n,m,diag);
        System.out.println(sk);
    }
    public static String sqrMat(int [][]mat, int n, int m,int diag[])
    {
        if(!(n==m)){
            return "NO";
        }
        int k=0;
        for(int i=0;i<mat.length;i++){
            for(int j=0;j<mat[i].length;j++ ){
                if(i==j){
                    diag[k]=mat[i][j];
                    k++;
                }
            }

        }
        return "yes" + "\n"+ Arrays.toString(diag) ;
    }
}
