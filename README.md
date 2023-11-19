kfz

    public class Kfz {
    private int sitze;
    private int tankInhalt;
    private float verbrauch;

    public Kfz(int sitze, int tankInhalt, float verbrauch) {
        this.sitze = sitze;
        this.tankInhalt = tankInhalt;
        this.verbrauch = verbrauch;
    }

    public float reichweite() {
        return tankInhalt / verbrauch * 100;
    }

    public float spritVerbrauch(int km) {
        return verbrauch * km / 100;
    }
    }



--------------------------------------------------------------------------------------------------------------------------

kfzDemo 

        public class KfzDemo {
        public static void main(String[] args) {
        KfzV0 minivan = new KfzV0();
        minivan.sitze = 6;
        minivan.tankInhalt = 70;
        minivan.verbrauch = 14;

        float reichweite = minivan.reichweite();
        System.out.println("Mögliche Reichweite des Minivans: " + reichweite + " km");
    }
    }


--------------------------------------------------------------------------------------------------------------------------


kfzV0

    public class KfzV0 {
    public int sitze;
    public int tankInhalt;
    public float verbrauch;

    public float reichweite() {
        return tankInhalt / verbrauch * 100;
    }

    public float spritVerbrauch(int km) {
        return verbrauch * km / 100;
    }
    }







--------------------------------------------------------------------------------------------------------------------------


KonstruktorDemo


    public class KonstruktorDemo {
    public static void main(String[] args) {
        Kfz minivan = new Kfz(6, 70, 14);
        Kfz sportwagen = new Kfz(2, 45, 11);

        System.out.println("Spritverbrauch Minivan (252 km): " + minivan.spritVerbrauch(252) + " Liter");
        System.out.println("Spritverbrauch Sportwagen (252 km): " + sportwagen.spritVerbrauch(252) + " Liter");
    }
    }

--------------------------------------------------------------------------------------------------------------------------
lkw

    public class Lkw extends Kfz {
    private int ladeFlaeche;
    private boolean hatAnhaenger;

    public Lkw(int sitze, int tankInhalt, float verbrauch, int ladeFlaeche, boolean hatAnhaenger) {
        super(sitze, tankInhalt, verbrauch);
        this.ladeFlaeche = ladeFlaeche;
        this.hatAnhaenger = hatAnhaenger;
    }

    @Override
    public float spritVerbrauch(int km) {
        return super.spritVerbrauch(km) + 1;
    }
}

--------------------------------------------------------------------------------------------------------------------------

LkwDemo

    public class LkwDemo {
    public static void main(String[] args) {
        Kfz sportWagen = new Kfz(2, 45, 11);
        Lkw magirus = new Lkw(2, 45, 11, 30, true);

        System.out.println("Verbrauch SportWagen (252 km): " + sportWagen.spritVerbrauch(252) + " Liter");
        System.out.println("Verbrauch Magirus (252 km): " + magirus.spritVerbrauch(252) + " Liter");
    }
    }

--------------------------------------------------------------------------------------------------------------------------

ReturnDemo

    public class ReturnDemo {
    public static void main(String[] args) {
        KfzV0 minivan = new KfzV0();
        minivan.sitze = 6;
        minivan.tankInhalt = 70;
        minivan.verbrauch = 14;

        System.out.println("Reichweite von Minivan: " + minivan.reichweite() + " Kilometer");

        KfzV0 sportwagen = new KfzV0();
        sportwagen.sitze = 2;
        sportwagen.tankInhalt = 45;
        sportwagen.verbrauch = 11;

        System.out.println("Reichweite von Sportwagen: " + sportwagen.reichweite() + " Kilometer");
    }
    }

--------------------------------------------------------------------------------------------------------------------------

SpritDemo

    public class SpritDemo {
    public static void main(String[] args) {
        KfzV0 minivan = new KfzV0();
        minivan.sitze = 6;
        minivan.tankInhalt = 70;
        minivan.verbrauch = 14;

        float verbrauchMinivan = minivan.spritVerbrauch(252);
        System.out.println("Spritverbrauch von Minivan für 252 km: " + verbrauchMinivan + " Liter");

        KfzV0 sportwagen = new KfzV0();
        sportwagen.sitze = 2;
        sportwagen.tankInhalt = 45;
        sportwagen.verbrauch = 11;

        float verbrauchSportwagen = sportwagen.spritVerbrauch(252);
        System.out.println("Spritverbrauch von Sportwagen für 252 km: " + verbrauchSportwagen + " Liter");
    }
    }    

--------------------------------------------------------------------------------------------------------------------------


ZweiKfz

 
     public class ZweiKfz {
    public static void main(String[] args) {
        KfzV0 minivan = new KfzV0();
        minivan.sitze = 6;
        minivan.tankInhalt = 70;
        minivan.verbrauch = 14;

        KfzV0 sportwagen = new KfzV0();
        sportwagen.sitze = 2;
        sportwagen.tankInhalt = 45;
        sportwagen.verbrauch = 11;

        System.out.println("Reichweite Minivan: " + minivan.reichweite() + " km");
        System.out.println("Reichweite Sportwagen: " + sportwagen.reichweite() + " km");
    }
    }
