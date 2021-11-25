סקירה ספרותית:
מאמר ראשון-
הסבר כללי על המעבר ממעלית טיפשה לחכמה, השינויים בטכנולוגיה אשר מאפשרים את 
ההתקדמות וייעול הזמנים ולמה הם הכרחיים: 
https://www.popularmechanics.com/technology/infrastructure/a20986/the-hidden-
 /science-of-elevators
מאמר שני- 
בעיה עם מעלית אחת, הסבר מינימלי על איך המעלית עובדת עם מעלית אחת: 
https://elevation.fandom.com/wiki/Elevator_algorithm
מאמר שלישי-
ניסיון לפתרון הבעיה עם אלגוריתם חישובי)מתמטיקה פשוטה( והגבלות מסוימות על מנת לתכנן 
בהתאם- 
/https://austingwalters.com/everyday-algorithms-elevator-allocation
מאמר רביעי-
ניסיון למזעור זמנים של הגעת מעלית לנקודת קריאה על ידי מציאת נקודת ההצבה האופטימלי: 
https://idogreenberg.neocities.org/linked%20files/Articles/Elevators%20weighting%20time
%20optimization.pdf
מאמר חמישי-
ניסיון לפתרון הבעיה על ידי מערכת מורכבת אלגוריתם בינה מלאכותית אשר מקבלת החלטות 
עצירה בהתאם לנתונים התחלתיים על נקודות עומס ונקודות קריאה קיימות בבניין ולפיכך שילוח 
המעליות: 
https://www.cs.huji.ac.il/~ai/projects/2014/The_intelevator/files/report.pdf
אלגוריתם אונליין: 
נתבונן באלגוריתם שנועד לבצע אופטימיזציה בזמן ההמתנה לנוסעים במעליות חכמות . 
באלגוריתם זה התייחסנו למ מד הזמן שכן זהו הנתון אותו התבקשנו לשפר ולבצע בצורה הטובה 
ביותר על מנת להיטיב עם הנוסעים והזמן שלהם . 
נראה כי על מנת לשנות את המערכת מ"טיפשה" ל"חכמה" יש צורך להפעיל חישובים והתייחסויות 
שונות, בשונה ממערכת "טיפשה" . 
מכאן ניתן לעבור לרעיון הכללי: 
על מנת לשמור על ממוצע זמן שלא יפגע באף אחד מהנוסעים נרצה לשמר נוסחת זמן בכל קריאה 
חדשה, שתמצא את הזמן הנמוך ביותר למסלולים האפשריים העומדים בפני הקריאה ותבחר את 
הטובה ביותר-זאת עם הזמן הכי נמוך. 
לזמנים אלו צריך להוסיף את הגבלות המטלה ,כיווני קריאה ביחס לכיוון מעלית וכו' .
בכך , נוכל למצות את האפשרויות העומדות בפנינו בתוך הנוסחה לחישוב זמן ,אשר מחפשת את 
הזמן הקצר ביותר למסלול המעלית באשר לקריאה הנוכחית ומרכיבי הנוסחה לחישוב הם כדלהלן:
נגדיר את הפעולות הבאות לפי מרכיב הזמן שהם לוקחות ונשתמש בהם: 
פתיחת דלתות, סגירת דלתות , תחילת תנועה , עצירת תנועה , נסיעה מנקודת קריאה ליעד.
1 .במידה והמעלית במצב מנוחה: 
נסיעה מנקודת המוצא של המעלית למקור הקריאה, זמן פתיחת דלתות, זמן סגירת דלתות, 
נסיעה ליעד המבוקש, זמן פתיחת דלתות. 
2 .במידה והמעלית בתנועה: 
א. מעלית לא בכיוון הקריאה-ממשיכה ליעד שלה. 
ב. מעלית בכיוון הקריאה ביחס לכיוון הקריאה אבל עברה את הקומה הרצויה-ממשיכה 
ליעד שלה.
ג. מעלית עברה את קומת הביניים-ממשיכה ליעד שלה. 
3 .במידה והמעלית בתנועה, אותו כיוון ועוד לא עברה את נקודת הקריאה)נבנה לטובת כך 
מבנה נתונים שישמור את הקריאות(: 
א. חשב זמן נסיעה מנקודת מוצא המעלית לנקודת הקריאה, חשב פתיח ת דלתות, סגירת 
דלתות, זמן נסיעה לנקודת היעד, חשב פתיח ת דלתות, סגירת דלתות. 
4 .במידה ואין מעלית או אפשרות לפניות: 
חשב זמן סיום קריאה קודמת. 
ותוסיף:
א. אם באותה קומה חשב סגירת דלתות, חשב זמן נסיעה ליעד המבוקש וזמן סגירת 
דלתות. 
ב. אחרת הוספה של זמן סגירת דלתות, נסיעה מנקודת מוצא למקור הבקשה, זמן פתיחת 
דלתות, זמן סגירת דלתות, נסיעה ליעד המבוקש, זמן פתיחת דלתות. 
מתוך החישובים שבוצעו על כל המעליות נבחר בזמן הנמוך ביותר ובמקביל גם למעלית העמוסה הכי 
פחות, בכך נקבל אופטימיזצי ה וחלוקה לממוצע את הזמן שמתחלק פר כל נוסע במעלית.
לפונקציית ה– cmd נפצל למקרים השונים-
• מצב מנוחה של המעלית 
• מצב ירידה של המעלית
• מצב עלייה של המעלית
ובכך נקבל את הקריאות ונפעיל את המעליות בהתאם למצב המעלית ואח"כ תבדוק את 
המעלית הטובה ביותר לקראת משימת הקריאה ובכך נבנה את המסלול של כל מעלית על פי 
הקריאות שלה. 
אלגוריתם אופליין: 
במצב של אופליין הקלט מתקבל במערכת מראש ועל כן ניתן להיערך אחרת לקריאות.
נרצה לעשות התאמות על פי הקלט שנקבל מראש, בצורה הזאת נרצה לה תבסס על הרעיון 
של המאמר שהצגנו למעלה, מ זעור זמנים בהצבת מעליות בכך שנשלח את המעלית מראש 
לנקודת מקור הקריאה.
נפעל באופן דומה לאלגוריתם אונליין לחישוב זמני הנסיעה אך אם סייג אחד. 
לאור העובדה כי זמני הקריאות ידועות לנו נוכל לבדוק האם להשתמש במעלית במנוחה או 
במעלית שכבר בתנועה באזור )הכי קרוב וזמן מינימלי למילוי המשימה( ביחס לקריאה 
הבאה ובכך להיערך הלאה לקריאה הבאה,לגרום להורדת הזמן באופן משמעותי לאור 
הסיבה כי ניתן לקצר את זמן ההמתנה של הקריאה הבאה בתור.
משמעות הדבר היא כי בכל קריאה אנו בודקים את הזמן הקצר ביותר לקריאה הנוכחית וגם 
לקריאה הבאה, בכך נייעל את הזמנים של כל המערכת. 
 :UML
 
 
 
-JUNIT
כתרחישים לבדיקת מערכת המעלית נרצה לבצע מספר תרחישי קצה 
• בדיקה כי המעלית יודעת להבדיל בין למעלה ולמטה- קריאות צמודות מתחלפות, כלומר 
קריאה יורדת וקריאה הבאה עולה וכן האלה על מנת לראות את שהמערכת עובדת במקביל 
ולא אוספת את כולם . 
• בדיקה שכל המעליות יכולות להיות מופעלות-הפעלת קריאות בתזמון קצר לבדיקה מי אוסף 
אותן.
• בדיקה לצמצום זמני המתנה על ידי כללי חישוב- עומס קריאות במרחב הנסיעה על מנת 
לראות ייעול מערכת ומזעור זמני המתנה חלוקת עומסים בין כל המעליות. 
• בדיקה לצורך סיום קריאות המעלית- שליחת מקבץ קריאות והמתנה לוודא שכל קריאה 
מגיעה ליעדה והקריאה נסגרת.
• ניתן לבצע באותו אופן שילוב של תרחישים על מנת לבדוק את הכל במקביל , כלומר חלוקת 
עומס ווידוא סיום קריאות, הפעלת מעליות וכיוונים מעליות בהתאם. 