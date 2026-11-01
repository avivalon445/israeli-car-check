# בדיקת רכב לפני שקונים

סקיל לקלוד שבודק רכב יד שנייה לפי מספר רישוי, מתוך הנתונים הרשמיים של משרד התחבורה.

הבדיקה מכסה רישום, טסט, היסטוריית קילומטרים, דגלים של שינוי מבנה או צבע, היסטוריית בעלויות, וקריאות לתיקון בטיחותי מהיצרן שעוד לא בוצעו. בסוף מקבלים דגלים אדומים, שאלות למוכר וטיעונים למיקוח.

## תוכנית בתשלום

ב-claude.ai: Customize › Plugins › Add › Add marketplace. מדביקים את הקישור לריפו:

`https://github.com/avivalon445/israeli-car-check`

לוחצים Add, מוסיפים את התוסף israeli-car-check, ואז Connect לקונקטור.

ב-Claude Code, מגרסה 2.1.275:

```
/plugin install israeli-car-check --marketplace avivalon445/israeli-car-check
```

## תוכנית חינם, התקנה קבועה

1. מוסיפים קונקטור מותאם: Customize › Connectors › Add custom connector, עם הכתובת `https://gateway.pipeworx.io/datagov-il/mcp`. אם שואלים על התחברות, בוחרים בלי התחברות (No sign in).
2. מפעילים code execution. בתוכניות אישיות: Settings › Capabilities › Code execution and file creation.
3. מורידים את הקובץ מהגרסה: https://github.com/avivalon445/israeli-car-check/releases/latest/download/israeli-car-check.zip
4. Customize › Skills › Upload a skill, ומעלים את ה-zip.

## תוכנית חינם, בדיקה מהירה

מוסיפים את אותו קונקטור, מפעילים Web search, ומדביקים:

```
עקוב אחרי ההוראות בקובץ הזה, מילה במילה:
https://raw.githubusercontent.com/avivalon445/israeli-car-check/main/skills/israeli-car-check/SKILL.md

תבדוק לי את הרכב מספר 12-345-67 לפני שאני קונה אותו
```

מחליפים את המספר במספר הרישוי של הרכב.

## מה לכתוב אחרי שהסקיל מותקן

```
תבדוק לי את הרכב מספר 12-345-67 לפני שאני קונה אותו
```

## מגבלות

הנתונים הרשמיים חלקיים. אין בהם תאונות או עיקולים. תמיד עושים גם בדיקה במוסך.

הקונקטור האנונימי של Pipeworx מוגבל לכ-50 קריאות ביום.

## קרדיטים

- [Pipeworx – mcp-datagov-il](https://github.com/pipeworx-io/mcp-datagov-il), הקונקטור המרוחק שבשימוש.
- [data-gov-il-mcp by DavidOsherdiagnostica](https://github.com/DavidOsherdiagnostica/data-gov-il-mcp), פרויקט הקוד הפתוח המקורי של MCP ל-data.gov.il.
- נתונים: "מקור: משרד התחבורה, data.gov.il". השימוש בנתונים כפוף לתנאי data.gov.il ולתנאי Pipeworx (לא מסחרי).
- נוצר על ידי CritiFly (Instagram).
