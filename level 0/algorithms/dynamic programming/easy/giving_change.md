## Giving change

   

    public static final int[] CENTIMES = {500, 200, 100, 50, 20, 10, 5, 2, 1};
    
        public static int[] monnaie(int centimes) {
            int[] rendu = new int[CENTIMES.length];
    
            for (int i = 0; i < CENTIMES.length; i++) {
                rendu[i] = centimes / CENTIMES[i];
                centimes %= CENTIMES[i];
            }
    
            return rendu;
        }
    
        public static void afficher(int[] rendu) {
            for (int i = 0; i < CENTIMES.length; i++) {
                if (rendu[i] != 0) {
                    System.out.printf("%d pièces de %d centimes\n", rendu[i], CENTIMES[i]);
                }
            }
        }