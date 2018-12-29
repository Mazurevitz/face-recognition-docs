![](media/image1.png){width="1.1in" height="1.1in"}

**[Silesian University of Technology ]{.smallcaps}**

**[Faculty of Automatic Control, Electronics\
and Computer Science]{.smallcaps}**

1.  ##### Final Project

    ##### (choose appropriate)

Implementation of face detection algorithms in video sequences

Author: Wojciech Mazur

Supervisor: PhD Michał Staniszewski

Consultant: PhD Name Surname

Gliwice, January 2019\
\
Załącznik Nr 2 do Zarz. Nr 97/08/09

**Oświadczenie**

Wyrażam zgodę/nie wyrażam\* zgody na udostępnienie mojej pracy
dyplomowej/rozprawy doktorskiej\*

.........................., dnia ..............................

.....................................................................

*(podpis)*

.....................................................................

*(poświadczenie wiarygodności podpisu przez Dziekanat)*

*\* właściwe podkreślić*

**Oświadczenie promotora**

Oświadczam, że praca „Implementation of face detection algorithms in
video sequences" spełnia wymagania formalne pracy dyplomowej
inżynierskiej.

+-----------------------------------+-----------------------------------+
| Gliwice, dnia                     | ................................. |
| ...........................       | ............                      |
|                                   |                                   |
|                                   | *(podpis)*                        |
+-----------------------------------+-----------------------------------+

Contents {#contents .TOCHeading}
========

[1. Introduction 1](#introduction)

[2. \[Problem analysis\] 5](#problem-analysis)

[3. Requirements and tools 9](#requirements-and-tools)

[4. External specification 12](#external-specification)

[5. Internal specification 15](#internal-specification)

[6. Verification and validation 18](#verification-and-validation)

[7. Conclusions 21](#conclusions)

[Bibliography i](#bibliography)

[List of abbreviations and symbols
ii](#list-of-abbreviations-and-symbols)

[Contents of attached CD-ROM iii](#contents-of-attached-cd-rom)

[List of Figures iv](#list-of-figures)

[List of Tables v](#list-of-tables)

**\
**

Introduction 
=============

This chapter contains following elements:

-   introduction into the problem domain,

-   settling of the problem in the domain,

-   objective of the thesis,

-   scope of the thesis,

-   short description of chapters,

-   clear description of contribution of the thesis's author -- in case
    > of more authors table with enumeration of contribution of authors.

> According to Maslow's Hierarchy of needs, safety is one of our most
> fundamental needs. Without it, it is hard to think about friends,
> relationships, accomplishments, or self-fulfillment. Over the last few
> years it can be observed, that the biological identification is rising
> in its popularity. There are new ways found to utilize our biological
> footprints. What we can also notice, is that most of the use cases
> revolves around security, and for a good reason. Fingerprints are used
> to unlock locks for decades. Fingerprint scanners have also found a
> way to consumer electronics. We can't imagine a world where we can't
> secure our smartphone or notebook just with a password. Fingerprint
> scanners have expended rapidly when it comes to smartphones and made
> our lives better.
>
> But it's not the only way we are trying to secure our privacy,
> including our increasingly valuable resource, which is data. We have
> developed ways to recognize people by other features like iris, or
> even from a face in general, using different kinds of sensors.
> Cameras, infrared light sensors to depth detectors that remember given
> points on a face. And everything happens within a blink of an eye.
>
> What we want to do apart from protecting our data, is something that
> we crave to do since beginning of the humanity. We want to protect
> ourselves. We want to feel safe and comfortable, it is, in fact,
> required, as stated previously.
>
> One of the main issues arising in recent years, is public safety and
> detection of dangerous people. We can observe increasing activity of
> terrorism in a lot of European countries. The awareness of people is
> also increasing, we are learning that prevention is better that
> treatment. National safety agencies recognize most of European
> countries at least on moderate threat of terrorism. A lot of countries
> are considered even as a high threat for regular travelers. This is
> something that needs to be addressed as quickly as possible, and we
> need to work on the technology, that can be effectively applicated for
> new solutions.
>
> Main goal of this thesis is to implement face detection algorithms,
> both with the face recognition. This could provide us with useful
> tools to analyze and examine, for example video footages that are
> collected every day on thousands of city cameras around the globe. We
> can use that existing architecture, not only to look for people that
> have already broke the law, but also to prevent crime. Simple camera
> system doesn't provide us with the possibility of detecting the face.
> We would need to do that manually which is a complicated and tedious
> work, that not every person is able to do. The main focus is to
> accomplish filtering dangerous, or at least for some reason crucial
> for safety people, implementing algorithms that detect and recognize
> their faces.

**\
**

\[Problem analysis\]
====================

This chapter contains following elements:

-   problem analysis,

-   state of the art, problem statement,

-   literature research (all sources in the thesis have to be referenced
    > \[1, 2, 4, 3\]),

-   description of existing solutions (also scientific ones, if the
    > problem is scientifically researched), algorithms, location of the
    > thesis in the scientific domain.

Requirements and tools 
=======================

This chapter contains following elements:

-   functional and nonfunctional requirements,

-   use cases (UML diagrams),

-   description of tools,

-   methodology of design and implementation.

.

External specification 
=======================

This chapter contains following elements:

-   hardware and software requirements,

-   installation procedure,

-   activation procedure,

-   types of users,

-   user manual,

-   system administration,

-   security issues,

-   example of usage,

-   working scenarios (with screenshots or output files).

The entire document should contain references to the illustrations
contained therein (Fig. 4.1).

  ![](media/image2.png){width="3.0625in" height="2.46875in"}
  ------------------------------------------------------------
  Fig.4.1. *The variation funkstioni*

Internal specification
======================

This chapter contains following elements:

-   concept of the system,

-   system architecture,

-   description of data structures (and data bases),

-   components, modules, libraries, resume of important classes (if
    > used),

-   resume of important algorithms (if used),

-   details of implementation of selected parts,

-   applied design patterns,

-   UML diagrams.

A short code insertion in the text line is possible, e.g. class Main.
Longer fragments should be written in *Courier* or *Courier New* font
size 10 in frames (Listing 4.1) with a space between the lines of the
value 1. All lines of code should be numbered so that they can be
referenced in the text of the document.

*Listing* *1. Generating random numbers*

+----+--------------------------------------------------------+
| 1  | **package** polsl.iinf.lab;                            |
|    |                                                        |
| 2  | **import** java.util.Random;                           |
|    |                                                        |
| 3  | **public** **class** Main {                            |
|    |                                                        |
| 4  | **public** **static** **void** main(String\[\] args) { |
|    |                                                        |
| 5  | Random r = **new** Random();                           |
|    |                                                        |
| 6  | // drawing a number from the range 1..10               |
|    |                                                        |
| 7  | **int** a = r.nextInt(10 + 1);                         |
|    |                                                        |
| 8  | System.*out*.println(a);                               |
|    |                                                        |
| 9  | // drawing a number from the range -5..15              |
|    |                                                        |
| 10 | System.*out*.println(r.nextInt(21) - 5);               |
|    |                                                        |
| 11 | }                                                      |
|    |                                                        |
| 12 | }                                                      |
|    |                                                        |
| 13 |                                                        |
|    |                                                        |
| 14 |                                                        |
|    |                                                        |
| 15 |                                                        |
|    |                                                        |
| 16 |                                                        |
|    |                                                        |
| 17 |                                                        |
+----+--------------------------------------------------------+

Verification and validation
===========================

This chapter contains following elements:

-   testing paradigm (eg. V model),

-   test cases, testing scope (full / partial),

-   detected and fixed bugs,

-   results of experiments (optional).

Conclusions
===========

This chapter contains following elements:

-   achieved results with regard to objectives of the thesis and
    > requirements,

-   path of further development (eg. functional extension . . . ),

-   encountered difficulties and problems.

Bibliography {#bibliography .ListParagraph}
============

+-----------------------------------+-----------------------------------+
| \[1\]                             | Name Surname, Name Surname.       |
|                                   | *Webpage title*.                  |
|                                   | http://adres/w/sieci.html         |
|                                   | \[access date: 2018-09-30\].      |
+===================================+===================================+
| \[2\]                             | Name Surname, Name Surname.       |
|                                   | *Title of a book*. Publisher,     |
|                                   | Warsaw, 2017.                     |
+-----------------------------------+-----------------------------------+
| \[3\]                             | Name Surname, Name Surname. Title |
|                                   | of an article in the journal.     |
|                                   | *Journal title*,                  |
|                                   | 157(8):1092--1113, 2016.          |
+-----------------------------------+-----------------------------------+
| \[4\]                             | Name Surname, Name Surname, Name  |
|                                   | Surname. Title of a conference    |
|                                   | article. In *Conference title*,   |
|                                   | pages 5346--5349, 2006.           |
|                                   |                                   |
|                                   | .                                 |
+-----------------------------------+-----------------------------------+

List of abbreviations and symbols {#list-of-abbreviations-and-symbols .ListParagraph}
=================================

  *DNA*   deoxyribonucleic acid
  ------- -------------------------
  *MVC*   model--view--controller
  *N*     cardinality of data set

Contents of attached CD-ROM {#contents-of-attached-cd-rom .ListParagraph}
===========================

The thesis is accompanied by a CD-ROM containing:

-   thesis (PDF file),

-   source code of applications,

List of Figures {#list-of-figures .ListParagraph}
===============

List of Tables {#list-of-tables .ListParagraph}
==============
