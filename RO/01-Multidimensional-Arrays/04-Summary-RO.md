[slide hideTitle]
# Rezumat


# În această lecție ai învățat:

- Ce este o Matrice Multidimensională?
     - matricele pot avea mai multe dimensiuni, de ex. matrice

```java
int[][] intMatrix = new int[3][];

```

- Crearea și Inițializarea

```java 
int[][] matrix = {
  {1, 2, 3, 4}, // row 0 values
  {5, 6, 7, 8}  // row 1 values
};
```

- Manipularea unei Matrice
    - accesarea elementelor din `Matrice 2D`
    ```java
    int [][] array = new int [5][5];
    array[0][0]  // the first element of the matrix
     ```

    - obținerea valorii elementului
    ```java live
    int[][] matrix = {
      {1, 2, 3, 4}, 
      {5, 6, 7, 8} 
    };

    int element = matrix[1][2]; 
    System.out.println(element);
    ```

    - setarea valorii elementului
    ```java 
    int[][] matrix = {
         {1, 2, 3, 4}, // row 0 values
         {5, 6, 7, 8}  // row 1 values
    };
    for (int row = 0; row < matrix.length; row++) {
       for (int col = 0; col < matrix[row].length; col++) {
           // setting all elements values to 1
           matrix[row][col] = 1;
       }
    }
    ```
    
- Citirea și Tipărirea unei Matrice

## În lecția următoare, veți învăța: 

- Sets:
    - HashSet\<E\>
    - TreeSet\<E\>
    - LinkedHashSet\<E\>
- Maps:
    - HashMap\<K, V\>
    - TreeMap\<K, V\>
    - LinkedHashMap\<K, V\>



[/slide]