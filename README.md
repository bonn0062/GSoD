# Google Summer of Docs: NumPy Beginner's Tutorial

Welcome to the repository for the Absolute Beginner's Guide to NumPy! This tutorial was built in collaboration with NumPy through Google Season of Docs 2019 . Please feel free to reach out with any ideas or suggestions!

In addition to GitHub, you can find the tutorial on [Towards Data Science](https://towardsdatascience.com/the-ultimate-beginners-guide-to-numpy-f5a2f99aef54).

If you're interested in the process of building this tutorial and the steps involved, take a look through the [pull request](https://github.com/numpy/numpy/pull/14546).


![NumPy_logo](images/NumPy_logo.svg)


Here's an exerpt from the Medium article introducing the project:

**From [Medium](https://towardsdatascience.com/what-do-you-want-to-see-in-the-numpy-docs-de73efb80375):**

## What do You Want to See in the NumPy Docs?
### Behind the scenes at NumPy and SciPy with Google Season of Docs

Season of Docs has begun!!!

## Google Season of Docs?

Google did an amazing thing by creating Season of Docs. It built real opportunities for technical writers to collaborate with open source organizations.
Season of Docs is a three-month mentoring program. It pairs technical writers with open source organizations. Writers have the opportunity to work with well-known and highly-regarded organizations. Open source organizations (who often don't have a budget for technical writers) have the opportunity to work with experienced technical writers to improve and expand their existing documentation.

It's pretty incredible.

The goal of Season of Docs is to provide a framework for technical writers and open source projects to work together towards the common goal of improving an open source project's documentation. For technical writers who are new to open source, the program provides an opportunity to gain experience in contributing to open source projects. For technical writers who're already working in open source, the program provides a potentially new way of working together. Season of Docs also gives open source projects an opportunity to engage more of the technical writing community.

During the program, technical writers spend a few months working closely with an open source community. They bring their technical writing expertise to the project's documentation, and at the same time learn about the open source project and new technologies.

The open source projects work with the technical writers to improve the project's documentation and processes. Together they may choose to build a new documentation set, or redesign the existing docs, or improve and document the open source community's contribution procedures and onboarding experience.

Together, we raise public awareness of open source docs, of technical writing, and of how we can work together to the benefit of the global open source community.

It's a win-win!

## What is NumPy?

At it's most basic level, NumPy is numeric, or numerical (**Num**) Python (**Py**).

**From the official documentation:**
"NumPy is the fundamental package for scientific computing in Python. It is a Python library that provides a multidimensional array object, various derived objects (such as masked arrays and matrices), and an assortment of routines for fast operations on arrays, including mathematical, logical, shape manipulation, sorting, selecting, I/O, discrete Fourier transforms, basic linear algebra, basic statistical operations, random simulation and much more."

It's a hugely important open source Python library. It's the core library for scientific computing in Python. It's useful in data science, machine learning, deep learning, artificial intelligence, computer vision, science, engineering, and more. It adds support for large, multi-dimensional arrays and matrices and a huge collection of high-level mathematical functions that can operate on the arrays.

The ancestor of NumPy (Numeric) was originally created by Jim Hugunin. By 2000, interest in creating a complete environment for scientific and technical computing was growing. In 2001, Travis Oliphant, Eric Jones, and Pearu Peterson merged code they had written and called the resulting package SciPy. In 2005, Travis Oliphant created NumPy. He did this by incorporating features of Numarray into Numeric with tons of modifications. In early 2005, he wanted to unify the community around a single array package. As a result, he released NumPy 1.0 in 2006. This project was part of SciPy. To avoid installing the large SciPy package just to get an array object, this new package was separated and called NumPy.

## What's SciPy?
It's scientific (Sci) Python (Py)! SciPy is a free and open source Python library. It's used for scientific computing and technical computing. It contains modules for optimization, linear algebra, integration, interpolation, special functions, FFT, signal and image processing, ODE solvers and other tasks common in science and engineering. SciPy uses NumPy arrays as the basic data structure. It has modules for various commonly used tasks in scientific programming. These tasks include integration (calculus), ordinary differential equation solving, and signal processing.

SciPy builds on the NumPy array object. It's part of the NumPy stack. The stack includes tools like Matplotlib, Pandas, and SymPy, and an expanding set of scientific computing libraries. Its users come from all fields of science, engineering and beyond. Python has one of the largest, if not the largest, scientific user communities. Similar communities are R, Julia and Matlab.

Still with me?

Google announced Season of Docs in March 2019. In April, open source organizations had the opportunity to apply to be a part of the program. Google announced the selected organizations on April 30. Technical writers were able to look over the list of 45 organizations and choose projects that interest them. They could submit up to three project proposals. From May 29-June 28, technical writer applications were open! After the application deadline was over, each organization selected the technical writing projects that they were interested in mentoring.

On August 6, Google announced the accepted writing projects!
The program received more than 700 technical writing project proposals from nearly 450 technical writers. Each organization was able to select one technical writer for an approved project. The NumPy/SciPy team, however, decided to go above and beyond by securing funding for an additional three writers outside of Season of Docs. The team believes so strongly in moving their documentation forward that they found additional funding. This allowed them to include three more writers under the same conditions as Season of Docs.

## Where did the funding come from?
NumPy received two grants that are kind of a package deal (you can read about them here and here). Funds were awarded by the Moore and Sloan foundations for $1.3M to the Berkeley Institute of Data Science (BIDS) to support the development of NumPy. The funding period runs from April 2018 to Oct 2020. (Stéfan van der Walt, a NumPy Steering Council member, agreed to provide the funds from that grant.)

Ralf Gommers, one of the core programmers behind NumPy and SciPy and the Director of Quansight Labs, is the point of contact for both organizations. Ralf is an incredible person, and he had this to say about Season of Docs:

"When I first saw the Season of Docs announcement, I loved the idea of the program - working with a tech writer would be both an interesting new experience for me personally, and potentially massively beneficial to NumPy and SciPy. So I spent a lot of effort on both writing a very engaging ideas page, and then following up with writers that showed interest. I probably had ~10 video calls, and many more email threads.
Then, it turned out that there was a lot of interest, and the quality of applicants and proposals was really high. I started thinking about how to not only get one or two 3-month projects running, but how to engage these writers in a way that would make them enjoy the experience enough to stay around after the project. One thing that came to mind was that people like working with like-minded others. However, we don't yet have technical writers - adding one to NumPy and one to SciPy may not be enough. So I decided to start building a documentation team. The ideas and people were there, so next what's needed is funding.

NumPy has a significant active grant, so I discussed the possibility of using some of that grant funding for the extra Season of Docs projects with Stéfan. Stéfan is awesome, and he also sees the value of both the proposed projects and of building a team of writers. So he agreed to reserve some funds for this purpose. So here we are today - excited to get started!"

## Who are the writers?
The writers selected for the NumPy/SciPy documentation projects are amazing, and you need to know who they are!

### Maja Gwozdz
The official technical writer selected by SciPy during Season of Docs is Maja Gwozdz. Her project proposal is called "User-oriented documentation and thorough restructuring." You can read all about it here, but essentially, Maja intends to work on the refactoring of the existing documentation, so that it would be easily accessible by users with different needs.
Maja has done some knockout research, which you can find here. She has not only had significant experience with SciPy, but she's well aware of what a difference great documentation and guides can make.

[Read more about Maja here!](https://towardsdatascience.com/scipy-meet-maja-gwozdz-61616cc35c08)

### Anne Bonner
Yours truly (yay!) was the official selection for NumPy, with the project proposal, "Making 'The Basics' a Little More Basic: Improving the Introductory NumPy Sections." Since there's nothing that makes me happier than helping beginners understand complex information and technologies, NumPy is the perfect challenge!
I'm excited to dig into the introductory NumPy materials to create something more accessible for people with little or no experience. NumPy is in such an interesting position: it's incredibly complex, but it's also one of the most important libraries for beginners who are interested in working with data. I'll be creating beginner-level documentation of basic concepts in NumPy that can function as a stepping stone for people who want to use NumPy, not necessarily study it.

### Shekhar Rajak
Shekhar Rajak was selected for "Numpy.org redesign and high-level documentation restructuring for end-user focus." His goals for the project include:
Designing and developing better UI for www.numpy.org
Enhancing and modifying the contents of www.numpy.org: NumPy User Guide, NumPy Benchmarking, F2Py Guide, NumPy Developer Guide, Building and Extending the Documentation, NumPy Reference, About NumPy, Reporting bugs and all other related to Development pages.
Adding contents about when to use NumPy and when to use XND, Dask array Python libraries, which provides similar APIs.
Preserving the Python API documentation.

### Brandon David
Brandon David was selected for his project "Improve the documentation of scipy.stats." Brandon plans to fill out missing functions as well as add examples and internal links. His goal is to clear up ambiguity and work through issues on GitHub.

### Christina Lee
Christina Lee was selected for her proposal, "SciPy documentation: Design, Usability and Content." She is a recent addition, and I'm looking forward to sharing her work with you soon!
Harivallabha Rangarajan
Harivallabha Rangarajan is planning to contribute to the documentation and complement the work of the writers selected for Season of Docs in any way he can. He's particularly interested in writing end-to-end tutorials for the scipy.stats module. He writes that "having more comprehensive tutorials will help users get a better idea of how and where the available methods may be used in the pipeline."

[Read about Christing here!](https://towardsdatascience.com/numpy-and-scipy-and-google-season-of-docs-oh-my-meet-christina-lee-d334c62c301)

**Welcome to Season of Docs!!!**

It's incredible to be involved in the inner workings of NumPy and SciPy. So far, we've been joining meetings with the team, getting to know the core players, and learning the workflow. I can't wait to keep you guys updated with our projects as they develop!
Photo by Pineapple Supply Co. from PexelsGet involved!

Now that you know the major players on the writing side, don't be afraid to reach out and let us know if there's information you want to see in the official documentation! Who knows, we might just be able to give you what you want to see.

If the idea of getting involved with open-source organizations interests you, get in there and start sharing! Don't wait for an invitation. Start contributing now! It's up to everyone to make the tech world an even more amazing place than it already is.
