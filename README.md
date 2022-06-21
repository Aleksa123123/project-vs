Console.ForegroundColor = ConsoleColor.White;
Console.WriteLine("koliko zelite osoba da unesete?");
int ljudi = int.Parse(Console.ReadLine());
Console.WriteLine("ok sada unesi ime za svaku osobu i prezime:");
string[] Imena = new string[ljudi];
string[] Prezimena = new string[ljudi];
int[] Godiste = new int[ljudi];
for (int i = 0; i < ljudi; i++)
{
    Console.ForegroundColor = ConsoleColor.Red;
    Console.Write("ime:");
    Imena[i] = Console.ReadLine();
    Console.ForegroundColor = ConsoleColor.Blue;
    Console.Write("prezime:");
    Prezimena[i] = Console.ReadLine();
    Console.Write("godiste:");
    Godiste[i] = int.Parse(Console.ReadLine());
}
Console.ForegroundColor = ConsoleColor.White;
Console.WriteLine("");
Console.WriteLine("Ispis:");
Console.WriteLine("");
for (int i = 0; i < ljudi; i++)
{
    Console.ForegroundColor = ConsoleColor.Yellow;
    Console.WriteLine($"{Imena[i]} {Prezimena[i]} {Godiste[i]}");
    Console.WriteLine("");
}
Console.ForegroundColor = ConsoleColor.White;
Console.WriteLine("da li zelite da stampate 1.imena 2.prezimena ili 3.godiste unesite broj po zelji");
Console.WriteLine("");
Console.ForegroundColor = ConsoleColor.White;
bool tacnoNetacno = true;
int zelja = 0;
while (tacnoNetacno)
{
    zelja = int.Parse(Console.ReadLine());
    if (zelja > 3)
    {
        Console.WriteLine("broj treba biti najvise do 3");
    }
    else if (zelja < 1)
    {
        Console.WriteLine("broj treba biti najmanje do 1");
    }
    else if (zelja == 1)
    {
        tacnoNetacno = false;
    }
    else if (zelja == 2)
    {
        tacnoNetacno = false;
    }
    else if (zelja == 3)
    {
        tacnoNetacno = false;
    }
}
Console.ForegroundColor = ConsoleColor.Red;
for (int i = 0; i < ljudi; i++)
    {
        if (zelja == 1)
        {
        Console.WriteLine("");
            Console.WriteLine(Imena[i]);

        }
        else if (zelja == 2)
        {
        Console.WriteLine("");
        Console.WriteLine(Prezimena[i]);
        }
        else if (zelja == 3)
        {
        Console.WriteLine("");
        Console.WriteLine(Godiste[i]);
        }
    }
Console.WriteLine("");
Console.ForegroundColor = ConsoleColor.DarkRed;
Console.WriteLine("Press any key to continue");
Console.ForegroundColor = ConsoleColor.Black;

