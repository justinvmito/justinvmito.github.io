---
layout: essay
type: essay
title: "Cleaning With Lint"
# All dates must be YYYY-MM-DD format!
date: 2025-02-13
published: true
labels:
  - Software Engineering
  - Coding Standards
  - Typescript
  - ESLint
---


Coding is fun. It is often challenging and requires the writer to put a lot of thought into it. While the concepts relevant to designing the program may be hard to come up with or understand at first, the thoughts and logic that emerge in response to the troubles are intriguing enough to beat out the frustration. Once I understand my goal and entertain a notion of how to get there, the writing and process of reaching the destination become entertaining, like a hobby. Hence, coding is fun, at least to me.
## Reading is Hard
While I enjoy writing code, the same cannot be said about reading it. It is difficult for me to visualize code when I am not actively in the process of writing it. As a result, reading and understanding code becomes just as, if not more, challenging than writing. Worse, it isn't fun, as it lacks the enjoyable mental process that come with designing. While already difficult, reading can be made even more arduous by errors like improper/non-standardized syntax, ugly code, and more. Problems like this is why the enforcement of coding standards is important.

<br>

<img width="200px" class="rounded float-start pe-4" src="../img/Lint/lint.jpg">

<br>

## Cleaning the Lint Filter
Over the past week, I have been writing typescript programs in VSCode under the watch of ESLint. ESLint has complained numerous, countless times about my code, forced me to add or remove hundreds of space characters or newlines, and made other objections which ultimately didn't change the functionality of my code. With or without ESLint, my program would have ran just fine. As tedious as it was to fix these benign errors, I must admit that ESLint's strict enforcement of coding standards was beneficial to my work. By forcing me to adopt and abide by a cleaner coding style, I have been able to better read my own code, an improvement which has enchanced my ability to debug and fix issues.
Following coding standards doesn't just clean up your code, it can also teach you a few tricks about the language.
<br>
Before installing ESLint, I utilized the variable type "any" often. On the occassion I had to deal with an array with contents of multiple types, I declared it to be of type "any." If a function's argument could take variables of different types, I also used "any." It always worked. Now imagine my surprise when ESLint gives me the error "warning  Unexpected any. Specify a different type  @typescript-eslint/no-explicit-any." I took to the internet to find out how to resolve this error, and in the process learned about the "unknown" variable type. Compared to "any," "unknown" has the same use cases, but notably is able to be type-checked, while "any" can not. Now, I use "unknown" instead of "any," thanks to ESLint. 

In the future, I will happily continue to use ESLint in my Typescript endeavours. I hope to be able to naturally write in ways that abide by common coding standards, and to learn more about Typescript and programming at the same time. Lint likes to clump up; hopefully ESLint will make sure my errors won't.
