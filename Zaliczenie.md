import java.util.Scanner;

public class oblicznie {

	public static void main(String[] args) {
		int a1;//Zmienne do przechowywania wartości funckji
		int a2;
		int b1;
		int b2;
		int c1;
		int c2;
		double az;// Zmienne do przechowywania wartości obliczeń.
		double bz;
		double cz;
		double delta;
		double pierw;
		double x1;
		double x2;
		double całka;
		double wynik = 0;
		double całka2;
		Scanner scan = new Scanner(System.in); //Tworzenie klasy Scanner.
		System.out.println("Podaj wartość a1");
		a1 = scan.nextInt();// Pobieranie danych od użytkownia.
		if(a1 == 0)
		{
			System.out.println("Funkcja nie jest kwadratowa");		
		}
		else
		{	
		System.out.println("Podaj wartość a2");
		a2 = scan.nextInt();
		if(a2 ==0 )
		{
			System.out.println("Funkcja nie jest kwadratowa");
		}
		else{
		System.out.println("Podaj wartość b1");
		b1 = scan.nextInt();
		System.out.println("Podaj wartość b2");
		b2 = scan.nextInt();
		System.out.println("Podaj wartość c1");
		c1 = scan.nextInt();
		System.out.println("Podaj wartość c2");
		c2 = scan.nextInt();
	    scan.close();
		
			az = a1-(a2);
			bz = b1-(b2);
			cz = c1-(c2);
			delta=(bz*bz) - (4*az*cz);
			if(delta < 0)
			{
				System.out.println("Delta < 0, funkcja nie ma miejsc zerowych");
			}
			else
			{
		    //Skorzystanie z funckji matematycznej do wyliczenia pierwiastka.	
			pierw = Math.sqrt(delta);
			// Obliczenie X1 i X2.
			x1 = (-bz - pierw) / (2 * az);
			x2 = (-bz + pierw) / (2 * az);
			// Obilczenie całków.
			całka = az*(1/3)*(x1*x1*x1)+bz*(1/2)*(x1*x1)+cz*x1;
			całka2 =az*(1/3)*(x2*x2*x2)+bz*(1/2)*(x2*x2)+cz*x2;
			// Obliczenie pola pomiędzy funkcjami.
			wynik = całka - całka2;	
			// Wyświetlanie wyników na ekran.
			System.out.format("Delta równia się: %.2f.\n ", delta);
			System.out.format("Pierwiastek z delty wynosi:%.2f.\n", pierw);
			System.out.format("X1 wynosi: %.2f.\n",  x1);
			System.out.format("X2 wynosi: %.2f.\n",  x2);
		
	System.out.format("Pole pomiędzy krzywymi wynosi: %.1f.\n", wynik);
	// Adrian Korpowski mechatronika I semestr. 
			  }
		   }
		}
	}
}
