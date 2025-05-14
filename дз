using System;

public class TextContainer
{
    private string[] lines;

    public TextContainer(string text)
    {
        lines = text.Split(new[] { "\r\n", "\r", "\n" }, StringSplitOptions.None);
    }

    public string this[int index]
    {
        get
        {
            if (index < 0 || index >= lines.Length)
                throw new IndexOutOfRangeException("Index out of range");
            return lines[index];
        }
    }

    public int LineCount
    {
        get { return lines.Length; }
    }
}

class Program
{
    static void Main()
    {
        string text = "Line one.\nLine two.\nLine three.";
        TextContainer container = new TextContainer(text);

        Console.WriteLine($"Line count: {container.LineCount}");
        for (int i = 0; i < container.LineCount; i++)
        {
            Console.WriteLine($"Line {i}: {container[i]}");
        }
    }
}
