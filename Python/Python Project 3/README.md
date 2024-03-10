Write a plot_function() that will:
- create a graph of the given quadratic function in the given argument range (the range of values on the OX axis);
- indicate its zeros (the specific values shown on the graph are shown next to the actual zeros (if the function has zeros);
- below the graph represented the minimum and maximum value of the function in the given argument range (a separate box below the OX axis);
- in the title it represented the formula of the function written in Latex;
- the space between the OX axis and the negative and positive values of the function to be in
transparent red and green respectively. The plot_function should take the following arguments:
- function = function form given as string (e.g. function = 'x**2-10')
- x_range = tuple defining the range of minimum and maximum values of the arguments (e.g.
x_range = (-10,10))
- num_points = number of arguments in given range (default 1000)
- show_roots = boolean (True or False) - parameter indicating whether to show the
zeroes.
Example of use:
plot_function (function = "x**2-10", x_range = (-10, 10), num_points = 1000, show_roots = True)
The above function should generate a graph of the function x**2-1 for arguments from 10 to 10, show the zero points and the minimum and maximum values of the function
