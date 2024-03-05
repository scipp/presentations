# No more spaghetti code: build reusable data pipeline with Sciline

## Abstract

Have you dealt with scary spaghetti code that was not written by yourself?
Or are you the one who wrote them?
Or do you want to have a visualization of the complicated data process but you do NOT want to use GUI-based frameworks?
If yes, [``sciline``](https://scipp.github.io/sciline) may be interesting to you.

In this talk, we will introduce the ``sciline`` as a complex data process development framework. ``Sciline`` provides an automatic assembly of the task graph that can compute desired outputs or visualize the process to compute them. It is inspired by dependency injection frameworks, and it relies on Python’s type-hinting. As long as your interfaces are correctly type-hinted, you can use them with ``sciline`` right away!

Sciline is developed for programmers and scientists to implement complicated data-processing workflows together in an efficient, clear and maintainable way.
With Sciline, our scientists can contribute to the development without knowing coding practices
and we, developers, can easily understand the process without asking what ``x`` means here and there!
