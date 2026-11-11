FROM python:3.11-slim  

#תקייה שבה הקונטיינר פועל
WORKDIR /app

#הגדרת משתני סביבה
ENV GREETING="health Winter"

# להעתיק את קובץ התלויות בנפרד שלא יהיה התקנה מחדש כל פעם
COPY requirements.txt .

#מריצה את הספריות שאותם צריך להתקין לפי מה שכתוב ב requirements
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

#איזה פורט לפתוח הקונטיינר בשביל שיוכלו לתקשר
EXPOSE 8000

#מה הקדה שצריך להריץ ב CMD
CMD ["python", "main.py"]
