# Insertion_Sort
O Insertion Sort ordena a lista inserindo cada elemento na posição correta, como em um jogo de cartas. Ele percorre a lista e desloca os elementos maiores para a direita, inserindo o atual na posição correta. É eficiente para pequenas listas ou quase ordenadas, com complexidade O(n²) no pior caso e O(n) no melhor.


public class InsertionSort {

    public static void insertionSort(int[] arr) {
        int n = arr.length;

        for (int i = 1; i < n; i++) {
            int key = arr[i];
            int j = i - 1;

            while (j >= 0 && arr[j] > key) {
                arr[j + 1] = arr[j];
                j--;
            }
            arr[j + 1] = key;

            System.out.print("Após o passo " + i + ": ");
            printArray(arr);
        }
    }

    public static void main(String[] args) {
        int[] arr = {65, 15, 26, 35, 78, 99, 45, 62, 16, 78}; 

        System.out.println("Array inicial:");
        printArray(arr);

        insertionSort(arr);

        System.out.println("\nArray ordenado:");
        printArray(arr);
    }

    public static void printArray(int[] arr) {
        for (int num : arr) {
            System.out.print(num + " ");
        }
        System.out.println();
    }
}
