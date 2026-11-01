# בדיקת רכב לפני שקונים

סקיל לקלוד שבודק רכב יד שנייה לפי מספר רישוי, מתוך הנתונים הרשמיים של משרד התחבורה.

הבדיקה מכסה רישום, טסט, היסטוריית קילומטרים, דגלים של שינוי מבנה או צבע, היסטוריית בעלויות, וקריאות לתיקון בטיחותי מהיצרן שעוד לא בוצעו. בסוף מקבלים דגלים אדומים, שאלות למוכר וטיעונים למיקוח.

## התקנה ב-claude.ai

claude.ai לא מתקין סקיל מכתובת של ריפו בגיטהאב. מעלים קובץ zip. המדריך הרשמי: [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

1. מוסיפים קונקטור מותאם: Customize → Connectors → Add custom connector, עם הכתובת `https://gateway.pipeworx.io/datagov-il/mcp`. אם מופיע קודם "+ Add", לוחצים עליו ואז על "Add custom connector". אם שואלים על התחברות, בוחרים בלי התחברות (No sign in).
2. מוודאים ש-code execution מופעל. בתוכניות אישיות: Settings → Capabilities → Code execution and file creation.
3. מורידים את [israeli-car-check.zip](https://github.com/avivalon445/israeli-car-check/raw/main/israeli-car-check.zip). אחר כך: Customize → Skills → + → Upload a skill, ומעלים את הקובץ. אם מופיע קודם "+ Create skill", בוחרים אותו ואז "Upload a skill".

אחרי ההעלאה מפעילים את הסקיל במתג.

## מה לכתוב לקלוד

```
תבדוק לי את הרכב מספר 12-345-67 לפני שאני קונה אותו
```

מחליפים את המספר במספר הרישוי של הרכב.

## מגבלות

הנתונים הרשמיים חלקיים. אין בהם תאונות או עיקולים. תמיד עושים גם בדיקה במוסך.

הקונקטור האנונימי של Pipeworx מוגבל לכ-50 קריאות ביום.

## קרדיטים

- [Pipeworx – mcp-datagov-il](https://github.com/pipeworx-io/mcp-datagov-il), הקונקטור המרוחק שבשימוש.
- [data-gov-il-mcp by DavidOsherdiagnostica](https://github.com/DavidOsherdiagnostica/data-gov-il-mcp), פרויקט הקוד הפתוח המקורי של MCP ל-data.gov.il.
- נתונים: "מקור: משרד התחבורה, data.gov.il". השימוש בנתונים כפוף לתנאי data.gov.il ולתנאי Pipeworx (לא מסחרי).
- נוצר על ידי CritiFly (Instagram).
