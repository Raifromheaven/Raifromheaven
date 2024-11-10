using System;
using System.Threading;

namespace BIRDS_OF_FEATHER
{
    class Program
    {
        static void Main()
        {
            string title = "\n";
            string lyrics = "\nAnd I don't know what I'm crying for" +
                            "\nI don't think I could love you more" +
                            "\nIt might not be long, but baby, I..." +
                            "\nI'll love you 'til the day that I die" +
                            "\n" +
                            "\n'Til the day that I die..." +
                            "\n'Til the light Leaves my eyes" +
                            "\n'Til the day that I die";

            TypeWriterEffect(title, 100, 500);
            TypeWriterEffect(lyrics, 50, 1000);
        }

        static void TypeWriterEffect(string text, int charDelay, int lineDelay)
        {
            foreach (char c in text)
            {
                Console.Write(c);
                Thread.Sleep(charDelay);

                if (c == '\n')
                {
                    Thread.Sleep(lineDelay);
                }
            }
        }
    }
}


