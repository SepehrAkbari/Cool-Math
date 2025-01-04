# Day's Date

This project explores two approaches to get the day of the week from a given date:

- Using Zeller's Congruence:

This method uses the following formula to calculate the day of the week, pretty cool!

$$
h = (q + \lfloor \frac{13(m+1)}{5} \rfloor + K + \lfloor \frac{K}{4} \rfloor + \lfloor \frac{J}{4} \rfloor - 2J)\mod 7
$$

[Zeller Notebook](https://github.com/SepehrAkbari/Cool-Math/blob/main/DaysDate/Zeller.ipynb)

- Using a Modular Arithmetic approach:

This is a bit more work, but interesting to think of and implement. The idea is to use the fact that the days of the week repeat every 7 days, so we can use the remainder of the division of the number of days since a known date to get the day of the week. We have to be careful with calculating offsets though, for example the leap years.

So if we wanna do the math, we can just count back, having the number of days in epcific months and the amount of leap years in mind to calculate the offset ($\delta d$). In this program though, I'm just using the `datetime` modules functions.

[Modular Notebook](https://github.com/SepehrAkbari/Cool-Math/blob/main/DaysDate/Modular.ipynb)

---

In either programs just enter the date in integers, and you'll get back the day of the week.

NOTE: In the year 1582 the Gregorian calendar was introduced by Pope Gregory XIII, so the algorithms will not be accurate for dates before that year. [Read More](https://www.britannica.com/story/ten-days-that-vanished-the-switch-to-the-gregorian-calendar)