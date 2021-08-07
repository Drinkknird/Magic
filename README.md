import java.util.Random;

public class MagicSquare {
    public static void main(String[] args) {
        Random random =new Random();
        int w =random.nextInt(50)+1;
        int x =random.nextInt(50)+1;
        int y =random.nextInt(50)+1;
        int z =random.nextInt(50)+1;
        Magicsquares(w,x,y,z);

    }

    static int Magicsquares(int w, int x, int y, int z) {
        int a = x - 1;
        int b = 7 - x + a;
        int c = 12 - z;
        int d = 10 - z + a;

        int array[][] = new int[4][4];
        for (int i = 0; i < 4; i++) {
            for (int j = 0; j < 4; j++) {
                if (i == 0 && j == 0) {
                    array[i][j] = w + a;
                } else if (i == 0 && j == 1) {
                    array[i][j] = x - a + b;
                } else if (i == 0 && j == 2) {
                    array[i][j] = y - c - b;
                } else if (i == 0 && j == 3) {
                    array[i][j] = z + c;
                } else if (i == 1 && j == 0) {
                    array[i][j] = z - a + d;
                } else if (i == 1 && j == 1) {
                    array[i][j] = y;
                } else if (i == 1 && j == 2) {
                    array[i][j] = x;
                } else if (i == 1 && j == 3) {
                    array[i][j] = w + a - d;
                } else if (i == 2 && j == 0) {
                    array[i][j] = x + c - d;
                } else if (i == 2 && j == 1) {
                    array[i][j] = w;
                } else if (i == 2 && j == 2) {
                    array[i][j] = z;
                } else if (i == 2 && j == 3) {
                    array[i][j] = y - c + d;
                } else if (i == 3 && j == 0) {
                    array[i][j] = y - c;
                } else if (i == 3 && j == 1) {
                    array[i][j] = z + a - b;
                } else if (i == 3 && j == 2) {
                    array[i][j] = w + c + b;
                } else if (i == 3 && j == 3) {
                    array[i][j] = x - a;
                }
            }
        }
            System.out.println("Array");
            for (int k = 0; k < 4; k++) {
                for (int j = 0; j < 4; j++) {
                    System.out.print("\t" + array[k][j]);
                }
                System.out.println();
            }
            int sum0 = 0;
            int sum1 = 0;
            int sum2 = 0;
            int sum3 = 0;
            int sum00 =0;
            int sum10 =0;
            int sum20 =0;
            int sum30 =0;
            for (int s =0;s < 4; s++){
                sum0 += array[0][s];
            }
            for (int s =0;s < 4; s++){
                sum1 += array[1][s];
            }
            for (int s =0;s < 4; s++){
                sum2 += array[2][s];
            }
            for (int s =0;s < 4; s++){
                sum3 += array[3][s];
            }
            for (int s =0;s < 4; s++){
                sum00 += array[s][0];
            }
            for (int s =0;s < 4; s++){
                sum10 += array[s][1];
            }
            for (int s =0;s < 4; s++){
                sum20 += array[s][2];
            }
            for (int s =0;s < 4; s++){
                sum30 += array[s][3];
            }

            System.out.println("ผลลรวมแถวที่1 : "+sum0);
            System.out.println("ผลลรวมแถวที่2 : "+sum1);
            System.out.println("ผลลรวมแถวที่่3 : "+sum2);
            System.out.println("ผลลรวมแถวที่4 : "+sum3);
            System.out.println("ผลลรวมหลักที่1 : "+sum00);
            System.out.println("ผลลรวมหลักที่2 : "+sum10);
            System.out.println("ผลลรวมหลักที่3 : "+sum20);
            System.out.println("ผลลรวมหลักที่4 : "+sum30);
        return x;
    }
}
