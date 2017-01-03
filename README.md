# Puzzle
¿Podrías decirnos cuál es el resultado de ejecutar el siguiente código? (suponiendo que la máquina tiene los recursos suficientes para terminar de ejecutarlo)
Se espera que obtengas como resultado un número concreto. Por favor no olvides comentarnos tu justificación y razonamiento aplicado para llegar al resultado.
Puzzle.java
import java.math.BigInteger;
class Puzzle {
    final static BigInteger M = new BigInteger("2017");

    private static BigInteger compute(long n) {
      String s = "";
      for (long i = 0; i < n; i++) {
          s = s + n;
      }
      return new BigInteger(s.toString()).mod(M);
    }

    public static void main(String args[]) {
      for (long n : new long[] { 1L, 2L, 5L, 10L, 20L, 58184241583791680L }) {
        System.out.println("" + n + ": " + compute(n));
      }
   }
}



Resultado parcial por consola
$ javac Puzzle.java
$ java Puzzle
1: 1
2: 22
5: 1096
10: 1197
20: 57
58184241583791680: ???
