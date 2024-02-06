using System;
class Analiza
{
    static void Main()
    {
        // inicializoji variablat (ndryshoret) në deklarime
        int numriIKalimeve = 0;
        int numriIDeshtimeve = 0;
        int numeruesiIStudenteve = 1;
        // procesoji 10 studentë duke përdorur
        // përsëritje të kontrolluar me numërues
        // (counter-controlled iteration)
        while (numeruesiIStudenteve <= 10)
        {
            // kërkoja shënimin hyrës përdoruesit dhe merre një vlerë
            Console.Write("Shkruaje rezultatin (1 = kalon, 2 = dështon): ");
            int rezultati = int.Parse(Console.ReadLine());
            // if...else është ndërfutur në urdhrin while
            if (rezultati == 1)
            {
                numriIKalimeve = numriIKalimeve + 1; // rrite numrin e kalimeve
            }
            else
            {
                numriIDeshtimeve = numriIDeshtimeve + 1; // rrite nr. e dështimeve
            }
            // rrite numeruesin e studentëve ashtu që cikli dikur përfundon
            numeruesiIStudenteve = numeruesiIStudenteve + 1;
        }
        // faza e përfundimit; përgatiti dhe shfaqi rezultatet
        Console.WriteLine(
       $"Kaluan: {numriIKalimeve}\nDështuan: {numriIDeshtimeve}");
        // përcaktoje se a kanë kaluar mbi 8 studentë
        if (numriIKalimeve > 8)
        {
            Console.WriteLine("Bonus për instruktorin!");
        }
    }
}
