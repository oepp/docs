## Fill in the blanks dto
### C#
```cs
    public class QuestionItem
    {
        public string Text { get; set; }

        public bool IsBlank { get; set; }
    }

    public class Question
    {

        public string Description = "Fill in the blanks to declare two variables of type int and display their sum to the screen.";

        public QuestionItem[] Items = new QuestionItem[]
        {
            new QuestionItem () { Text = "int x = 8;", IsBlank = false },
            new QuestionItem () { Text = "\n", IsBlank = false },
            new QuestionItem () { Text = "int", IsBlank = true },
            new QuestionItem () { Text = " y = 15;", IsBlank = false },
            new QuestionItem () { Text = "\n", IsBlank = false },
            new QuestionItem () { Text = "Console.Writeline(", IsBlank = false },
            new QuestionItem () { Text = "x", IsBlank = true },
            new QuestionItem () { Text = "+", IsBlank = true },
            new QuestionItem () { Text = "y);", IsBlank = false }
          };
    }
```
### Json
```json
{
  "description": "Fill in the blanks to declare two variables of type int and display their sum to the screen.",
  "items": [
    {
      "text": "int x = 8;",
      "isBlank": false
    },
    {
      "text": "\n",
      "isBlank": false
    },
    {
      "text": "int",
      "isBlank": true
    },
    {
      "text": " y = 15;",
      "isBlank": false
    },
    {
      "text": "\n",
      "isBlank": false
    },
    {
      "text": "Console.Writeline(",
      "isBlank": false
    },
    {
      "text": "x",
      "isBlank": true
    },
    {
      "text": "+",
      "isBlank": true
    },
    {
      "text": "y);",
      "isBlank": false
    }
  ]
}
```
