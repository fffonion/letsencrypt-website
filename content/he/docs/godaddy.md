---
title: "אישורי Let's Encrypt באירוח של GoDaddy"
slug: godaddy
top_graphic: 1
date: 2019-12-02
lastmod: 2019-12-02
---

{{< lastmod >}}

אנו מקבלים שאלות רבות בנוגע לשימוש ב־Let’s Encrypt עם GoDaddy. אם GoDaddy משמש אותך לטובת אירוח אתרים שיתופי, מאוד מסובך כרגע להתקין אישור של Let’s Encrypt, לכן איננו ממליצים כרגע להשתמש באישורים שלנו עם GoDaddy. זה קורה כיוון שב־GoDaddy אין תמיכה ב[פרוטוקול ACME](https://tools.ietf.org/html/rfc8555) להנפקה וחידוש אישורים אוטומטית. במקום, מציעים ב־GoDaddy חידוש אוטומטי עם אישורים משלהם, שהם [בתוספת תשלום](https://www.godaddy.com/web-security/ssl-certificate).

איננו ממליצים להשתמש באישורי Let’s Encrypt על ספקי אחסון שאינם מממשים באופן ישיר את פרוטוקול ACME כיוון שמשמעות הדבר היא שאי אפשר לחדש אישורים בצורה אוטומטית לגמרי. אנחנו חושבים שחידושים אוטומטיים הם חלק מאוד חשוב בשימוש באישורים. השימוש ברכיב תכנה כדי לחדש אוטומטית מוריד את הסבירות שתוקף האישור שלך יפוג מבלי שיוחלף. אם תוקף האישור שלך פג, זה מאוד מתסכל עבור המשתמשים כיוון שזה מונע מהם להגיע לאתר שלך.

כיוון שאנו מאמינים אדוקים בחידוש אוטומטי, אנו מתכננים את האישורים שלנו כך שייעשה בהם שימוש עם אוטומציה של ACME. אישור של Let’s Encrypt אמור להתחדש אוטומטית לאחר 60 יום, ויפסיק לעבוד לאחר 90 יום אם לא עבר חידוש.

אם, לאחר שהבנת את הבעיות שמוצגות כאן, החלטת שמעניין אותך לנסות לתחזק אישור של Let’s Encrypt על גבי אחסון משותף של GoDaddy, ישנן [הנחיות](https://www.godaddy.com/help/install-a-lets-encrypt-certificate-on-your-cpanel-hosting-account-28023) שסופקו על ידי GoDaddy. כדאי לזכור שמעקב אחר ההוראות האלו גוזל זמן רב ושיהיה עליך לחזור על כך כל 60 יום (לא כל 90 כפי שמצוין בעמוד המקושר).