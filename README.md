# numero_amstrong
calcular numero amstrong
import java.io.*;
class numero_amstrong {

	public static void main (String[] args) {
		public static int potencia (int base, int exponente) {
			int res = base;
			for (int i = 0; i < exponente-1; i++) {
			res = res *base;
			}
			return res;
			}
			public static int armstrong (int numero) {
			int cifra1 = numero/100;
			int cifra2 = (numero - 100 *cifra1) / 10;
			int cifra3 = numero - 100 * cifra1 - 10 * cifra2;
			int dat = potencia (cifra1, 3) + potencia(cifra2, 3) + potencia(cifra3,3);
			if (dat == numero) return 1;
			return 0;
			}
			
	public static void main (String[] args) throws IOException{
			int numero ;
			System.out.println ("Introduce un número: ");
			BufferedReader entrada = new BufferedReader(new InputStreamReader
			(System.in));
			numero = Integer.parseInt(entrada.readLine());
			if (armstrong(numero) == 1)
			System.out.println ("El número "+ numero+ " es un número Armstrong");
			else
			System.out.println ("El número "+ numero+ " no es un número Armstrong");

	}

}
