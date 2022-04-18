# User Date/Time Format

When setting the user format, the following sets of formatting characters are used:

* Day.
   * **d** — day of the month without leading zero.
   * **dd** — day of the month in the form of 2 digits.
* Day of the week.
   * **ddd** — day of the week in the abbreviated format ("Sun", "Mon", etc).
   * **dddd** — day of the week in the full format  ("Sunday", "Monday", etc).
      *Month.
   * **m** — number of the month without leading zero.
   * **mm** — number of the month in the form of 2 digits.
   * **mmm** — month in the abbreviated format ("Jan", "Feb", etc).
   * **mmmm** — month in the full format ("January", "February", etc).
* Year.
   * **y** or **yy** — year, 2 digits.
   * **yyyy** — year, 4 digits.
* Hours.
   * **h** — hours without leading zero.
   * **hh** — hours in the form of 2 digits.
* Minutes.
   * **n** — minutes without leading zero.
   * **nn** — minutes in the form of 2 digits.
* Seconds.
   * **s** — seconds without leading zero.
   * **ss** — seconds in the form of 2 digits.
* Milliseconds.
   * **z** — mlliseconds without leading zero.
   * **zzz** — mlliseconds in the form of 2 digits.

**Example:**

To represent '11.08.1917' date in the following form: "It was **August** **17**" the following formatting string is used: "It was **mmmm** **yy**".
