package sample;

public class ArrayFindingValues {
    public static void main(String[] args) {
        int[][] inputArray ={
                {1,2,3},
                {4,5,6},
                {7,8,9}
        };
        int[][] outputArray = returnColumnsAsRows(inputArray);
        for(int i=0; i<outputArray.length; i++){
            for(int j=0; j<outputArray[i].length; j++){
                System.out.print(outputArray[i][j]+ " ");
            }
            System.out.println();

        }
    }

    public static int[][] returnColumnsAsRows(int[][] arr) {
        int[][] resultArray = new int[arr[0].length][arr.length];
        for(int i=0; i<arr.length; i++){
            for(int j=0; j<arr[i].length; j++){
                resultArray[j][i]=arr[i][j];
            }
        }
        return resultArray;
    }
}
