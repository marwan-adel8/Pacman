# مشروع Pacman AI - بحث وتخطيط

## جامعة المنصورة - كلية الحاسبات والمعلومات

**القائمون على المشروع:**
- علي ياسر
- مروان السقا

---

## نبذة عن المشروع

ده مشروع لتطبيق خوارزميات البحث في الذكاء الاصطناعي. الفكرة إننا بنعلم Pacman إزاي يلاقي أحسن طريق في المتاهة عشان:
- يوصل لنقطة معينة
- ياكل كل النقاط البيضاء
- يزور الزوايا الأربعة
- يتجنب الأشباح

---

## الخوارزميات المستخدمة

| الخوارزمية | الوظيفة |
|------------|---------|
| DFS | يدخل في أول طريق لحد النهاية |
| BFS | يلاقي أقصر طريق بالخطوات |
| UCS | يلاقي أقل طريق بالتكلفة |
| A* | أسرع خوارزمية مع Heuristic |

---

## طريقة التشغيل

### المتطلبات
- Python 3.x
- Tkinter

### الأوامر الأساسية

```bash
python pacman.py
```

ده بيشغل اللعبة وانت تتحكم بيها بالأسهم أو WASD.

### تشغيل الخوارزميات

```bash

علشان تعمل run للعبه الاساسيه 

✅ python pacman.py

# 1️⃣ DFS — بيلاقي solution بس مش optimal
python pacman.py -l mediumMaze -p SearchAgent -a fn=dfs

# 2️⃣ BFS — أقصر مسار بس بيفتح nodes كتير
python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs

# 3️⃣ UCS — زي BFS بس يراعي الـ cost
python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs

# 4️⃣ A* — أحسنهم: أقصر مسار + أقل nodes
python pacman.py -l mediumMaze -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic
```

### مشاكل متقدمة

```bash
python pacman.py -l mediumCorners -p AStarCornersAgent
python pacman.py -l trickySearch -p AStarFoodSearchAgent
```

---

## الملفات الرئيسية

| الملف | الوظيفة |
|-------|---------|
| pacman.py | شغل اللعبة |
| search.py | فيه خوارزميات البحث |
| searchAgents.py | الوكلاء اللي بتحكم في Pacman |
| game.py | منطق اللعبة |
| util.py | هياكل البيانات (Stack, Queue, PriorityQueue) |
| layouts/ | المتاهات الجاهزة |

---

## الخيارات المتاحة

| الخيار | الوظيفة |
|--------|---------|
| -l | اختيار المتاهة |
| -p | اختيار الوكيل |
| -a | معاملات للوكيل |
| -z | تكبير أو تصغير |
| -t | وضع النص فقط |
| -q | وضع صامت |

---

## أمثلة

```bash
python pacman.py -l bigMaze -z 0.5
python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs
python pacman.py -l testSearch -p AStarFoodSearchAgent
```

---

تم إعداد المشروع كجزء من متطلبات مادة الذكاء الاصطناعي  
جامعة المنصورة - كلية الحاسبات والمعلومات
