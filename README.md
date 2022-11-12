# pkingston.xyz

Welcome to the repo for [pkingston.xyz](https://pkingston.xyz). It contains all of the files for my website, and documents my entire design and development process as a demonstration of competency for employers.

## Designing pkingston.xyz

To see the rationale for why I design my systems like this, scroll down to the **Design Philosophy** section.

### What data is needed?

For ease of understanding everything, I'll be starting with the top down approach of breaking my website into sub-websites and using a bottom up approach with each of those sub systems.

Broader system: Website

Subsystems:

- Homepage
- Portfolio page
- About me/contact page
- Blog
- Guestbook

#### Homepage

What data does the homepage need?

- My name
- A way to get to the portfolio page
- A way to get to the about me/contact page
- A way to get to the blog page
- A way to Guestbook

## Design philosophy

**_NOTE:_** I'm wording this as if it's either/or, but often the most sane way to do things is to break things down with top-down decomposition and then whenever it's time to write code do a bottom-up data oriented approach with the pieces of data you derive from the decomposition step. 

This project is designed with a *Bottom Up* and *Data Oriented* approach. Let's break down each.

### Bottom Up

So there are many ways of designing systems. These include, but are not limited to:

1. Roulette Design
2. Top Down
3. Bottom Up

#### Roulette Programming

Roulette programming is the process of just getting started on something and just seeing where things go. 

#### Top Down

The top down approach starts with the final product/intended outcome/complete system and iteratively decomposes it to smaller parts until the designer arrives at the basic procedures/data needed to program it. This is, as far as I'm concerned, a good approach for many things. However, I don't believe that it yields good programming results very often. 

This is because the thought process is foreign to computers. It begins with the high level abstraction instead of arriving at a simple, easy to reason about, and easy to explain domain-specific abstraction. 

So what's the alternative?

#### The Bottom Up approach

The Bottom-Up approach is the most sane approach to programming. Instead of beginning at the high level abstractions, it starts with the smallest unit of a system and composes each of these small components until the final product emerges out of the pieces.

The question that naturally follows is: What are the small pieces?

### Data Oriented

This is where data oriented design comes into play. There are, as far as I'm concerned, two sane approaches to programming.

* Procedure Oriented
* Data Oriented

#### Procedure Oriented

This is a fine approach. It begins with the question: What are all the actions the user can do with the system? 

This approach creates all of these operations and lets the data needed fall out of the design and composition of these procedures.

#### Data Oriented

Data Oriented design, however, begins with the data the program needs, and creates small functions and composes them to result in clear and declaratively designed systems.

It begins by asking "What data do I need?" Once it answers these questions it asks "How do I initialize this data?" and creates functions that generate the data to the desired initial states. It then asks "How does this data change throughout the course of the program?" and implements those functions on the data.

#### Why?

So why do we design systems using this approach?

1. state' = f(state)
2. ui = ui_fn(state)

It allows state to be immutable and changed as the result of high level functions that implement the state' = f(state) operations. 
It also allows the ui to be created incredibly easily. All you need in a ui is to render the easily accessible data. In the event of a high level state' = f(state) function, all you need to do is re-render the necessary parts of the ui.

