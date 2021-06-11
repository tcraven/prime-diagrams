# Prime Factor Radial Diagrams

This web page displays prime factor radial diagrams rendered using Javascript and SVG.

Each number is drawn as a sequence of nested radial graphs, using its prime factors to determine how many spokes to draw on each graph.

The code works as follows:
* For each number, a SVG definition is generated, which is either a single radial diagram if the number is prime, or a sequence of
nested radial diagrams if the number is not prime and has two or more prime factors
* Since the numbers are processed from smallest to largest, larger numbers need only reference the already defined diagrams for their
prime factors. For example, `18 = 2 x 3 x 3` becomes `2 x "3 x 3"`, where `"3 x 3"` was already defined earlier for `9 = 3 x 3`.

Since the page is rendered as SVG, it becomes slow to draw and runs out of memory beyond about 150 numbers.

Use the browser zoom function to view the individual diagrams in more detail.

This project was inspired by the following image: [https://disco.bu.edu/~tsl/prime-factor-chart-radial-200dpi.png](https://disco.bu.edu/~tsl/prime-factor-chart-radial-200dpi.png).
