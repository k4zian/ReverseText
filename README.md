# ReverseText
Text reversing console app.

Trying to learn something here!

```
static void Main(string[] args)
        {
            string closeApp = "x";
            Console.WriteLine("Welcome to the incredible text reversing application." +
                            "\nEnter any text below. Type 'x' to exit.");
            string tekst = "";
            while (!tekst.Equals(closeApp)) // Main loop
            {
                tekst = Console.ReadLine();

                while (tekst == "") // Exception handling for empty input
                {
                    Console.WriteLine("Nothing has been typed. Try again.");
                    tekst = Console.ReadLine();
                }

                Console.WriteLine(revert(tekst)); 
            }
        }

        static string revert(string input) // Core function
        {
            string output = "";
            input = input.Trim();
            for (int i = input.Length - 1; i >= 0; i--)
            {
                output += input.ElementAt<char>(i);
            }
            return output;
        }
```
