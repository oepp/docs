## Question DTO
### C#
```cs
    public class QuestionLine
    {
        public QuestionItem[] Items { get; set; }
    }

    public class QuestionItem
    {
        public string Text { get; set; }

        public bool IsBlank { get; set; }
    }

    public class Question
    {

        public string Description = "Fill in the blanks to declare two variables of type int and display their sum to the screen.";

        public QuestionLine[] Lines = new QuestionLine[]
        {
            new QuestionLine { Items = new QuestionItem[] { new QuestionItem() { Text = "int x = 8;", IsBlank = false } } },
            new QuestionLine { Items = new QuestionItem[] { new QuestionItem() { Text = "int", IsBlank = true }, new QuestionItem() { Text = " y = 15;", IsBlank = false } }},
            new QuestionLine { Items = new QuestionItem[] { new QuestionItem() { Text = "Console.Writeline(", IsBlank = false }, new QuestionItem() { Text = "x", IsBlank = true }, new QuestionItem() { Text = "+", IsBlank = true }, new QuestionItem() { Text = "y);", IsBlank = false } } }
        };
    }
```
### Json
```json
{
  "description": "Fill in the blanks to declare two variables of type int and display their sum to the screen.",
  "lines": [
    {
      "items": [
        {
          "text": "int x = 8;",
          "isBlank": false
        }
      ]
    },
    {
      "items": [
        {
          "text": "int",
          "isBlank": true
        },
        {
          "text": " y = 15;",
          "isBlank": false
        }
      ]
    },
    {
      "items": [
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
  ]
}
```

## LessonInfo DTO
### C#
```cs
	public enum LessonType
    {
        FillInTheBlanks
    }

    public class LessonInfo
    {
        public int Id { get; set; }
        public LessonType Type { get; set; }
        public string Title { get; set; }
        public string Description { get; set; }
        public byte[] Image { get; set; }
        public string Creator { get; set; }
        public DateTime CreationTime { get; set; }
    }

    public class LessonProvider
    {
        public LessonInfo[] GetPopularLessons = new LessonInfo[]
        {
            new LessonInfo { Id = 1, Type = LessonType.FillInTheBlanks, Title = "Java", Image = new byte[] {110, 125, 123}, Creator = "Alp Yuksel", CreationTime = new DateTime(2020, 5, 9) },
            new LessonInfo { Id = 5, Type = LessonType.FillInTheBlanks, Title = "C#", Image = new byte[] {37, 33, 120}, Creator = "Onur Tanrikulu", CreationTime = new DateTime(2020, 5, 8) }
        };


        public LessonInfo[] GetNewLessons = new LessonInfo[]
        {
            new LessonInfo { Id = 1233, Type = LessonType.FillInTheBlanks, Title = "Unity", Image = new byte[] {45, 55, 32}, Creator = "Emre Edemir", CreationTime = new DateTime(2020, 5, 10) },
            new LessonInfo { Id = 1, Type = LessonType.FillInTheBlanks, Title = "Java", Image = new byte[] {110, 125, 123}, Creator = "Alp Yuksel", CreationTime = new DateTime(2020, 5, 9) }
        };
    }
```
### Json
```json
{
  "getPopularLessons": [
    {
      "id": 1,
      "type": 0,
      "title": "Java",
      "description": "Introduction to Java",
      "image": "blob bytes will be here",
      "creator": "Alp Yuksel",
      "creationTime": "2020-05-09T00:00:00"
    },
    {
      "id": 5,
      "type": 0,
      "title": "C#",
      "description": "Introduction to C#",
      "image": "blob bytes will be here",
      "creator": "Onur Tanrikulu",
      "creationTime": "2020-05-08"
    }
  ],
  "getNewLessons": [
    {
      "id": 1233,
      "type": 0,
      "title": "Unity",
      "description": "Introduction to Unity",
      "image": "blob bytes will be here",
      "creator": "Emre Edemir",
      "creationTime": "2020-05-10"
    },
    {
      "id": 1,
      "type": 0,
      "title": "Java",
      "description": "Introduction to Java",
      "image": "blob bytes will be here",
      "creator": "Alp Yuksel",
      "creationTime": "2020-05-09"
    }
  ]
}
```
