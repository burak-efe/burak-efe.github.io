
---
title: MicroRant; It's Not Just Data And Processing
date: 2024-11-04
categories: [MicroRant]
tags: [DOD]     
---

I'm kind of sick of hearing the same phrase that every DOD evangelist parroting:
"Our job is Take Data -> Process Data -> Output data. Everything else unnecessary abstractions"

Sure buddy, everything as simple as this and your way of programming is most purest and holy way of possible.
Guess what, looks like every other domain also wasting their time with unnecesary abtractions too.
Architecture? Its all bloated, their job is taking rock -> put on another rock,
Banking? Take money -> Process Money -> output Money,
Government? Collect Tax -> ? -> Collect Tax.

So that's not makes sense right? Because complexity does not comes from the complexity of the most atomic part of the domain, instead it comes from the sum of all middle products that should be introduced to the solution that solves that specific problem.
For example you cannot just know or predict behaviour of every day objects by just knowing well the sub atomic particles plus main forces of the universe.
We need theorems, simplification, generalizations just to comprehend our problem domain or to be able to calculate in reasonable time.
For example think of the ray tracing algorithm, in theory its so simple:

For every pixel on the image shoot a ray from view direction,
bounce it around scene and accumulate the color information.

Its simple as that, but due to  high cost the operation, its not viable for real-time render even for monster GPUs.
That's way we need to introduce more and complexity 
(like RTAS with custom hardware, extensions on the  graphic api, new shader stages, denoisers, new rules on mesh topology)
 to our solution to create reasonable product.
 
 And there is no need to look at to a java codebase, even a basic C codebase has all of this middle products.
 Lets think one level upper of abstractions that many of the low level languages have;
 
 Data: Data on ram, data on disk, data on web, static data, global data, dat on heap, data on stack, data that need to be parsed, data that need to encrypted, data that cannot be trusted, 
 Metadata, data that just a view, data that need to be secure, data that point another data, data that point a function, 
 
 Processing: Functions, Methods, overloaded functions, functions that have implicit state, functions that mutate, functions that does not mutate, functions that allocate, functions that removes ownership or delete
 
 IO: mouse, keyboard, console, monitor, audio, web, file, another process
 
 and there are windowing apis, graphic apis, Operating System, UI libraries, standard libraries and so on that does not fit "just data and processing" idea.
 