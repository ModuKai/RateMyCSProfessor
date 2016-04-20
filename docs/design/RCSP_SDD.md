# [Rate My CS Professor][RCSP_Repo]

## Software Design Documentation
##### Product Version: 1.0
##### Document Version: 1.0
##### Date: 04-xx-2016

---

## Table of Contents
> 1. [Introduction](#introduction)
> 2. [Use Cases](#use_cases)
> 3. [Design Overview](#design_overview)
> 4. [User Interface Design](#user_interface_design)
> 5. [Architectural & Components Design](#arch_and_comp_design)
> 6. [Data Model](#data_model)
> 7. [Testing](#testing)
> 8. [Appendices](#appendices)

---

<a name="introduction"></a>
## 1. Introduction
> - [Goals & Objectives](#intro-goals_and_objectives)
> - [Scope](#intro-scope)
> - [Context](#intro-context)
> - [Constraints](#intro-constraints)

<p>
  The purpose of this software design document is to outline and carefully describe different aspects of the RateMyCSProfessor website through a developmental lens, primarily for developmental purposes. However it may also be used as not only a primer for anyone newly involved in the project, but as an updated reference to the current design model. Any API-related investigations are irrelevant here.
</p>
<p>
  Design decisions may change with solution iterations, and so there will consequently occur changes & updates to this document, with a revision history kept in the appendices.
</p>

---

<a name="intro-goals_and_objectives"></a>
- 1.1 Goals & Objectives

<p>
  The RateMyCSProfessor website is meant to be a domain-specific rating & feedback website in which both students and instructors may participate.
</p>
<p>
  It differs from other rating websites in that it allows a rater to go more in depth regarding his or her experience with the instructor, by virtue of domain-specificity. Whereas other websites are tailored to a general audience, where the rating template is too simplistic and often gives very limited useful information to curious students, a domain-specific rating website is specially capable of allowing a larger amount of relevant data to be inputted in a user-friendly way and consequently shared with students searching for exactly that type of specific information.
</p>
<p>
  It further distinguishes itself in terms of its profile and rating model; there is a tremendous amount of flexibility in store for users unseen at other rating websites, domain-specific or not.
</p>
<p>
  We hope to build a rating template that is highly user-friendly and, most importantly, as complete as possible in the sense of domain-specific information, with potentially optional inputs. Students can read other students ratings, and hopefully benefit mutually when a reader becomes a rater.
</p>
<p>
  One fundamental aspect of the rating environment planned at RCSP is that the instructor is not a victim. In RateMyCSProfessor, willing instructors will be provided the means to communicate with raters of their choosing, even capable of rating students with approval. What essentially happens is there begins to form an organized way for instructors to receive feedback from students as well as respond to that feedback publicly. Students may build prestigious profiles through objective and useful feedback, as well as recommendation-letter-like ratings from instructors.
</p>
<p>
  RateMyCSProfessor, in this way, becomes a communication board between instructors looking to improve and refine their teaching skills and standards, and students wanting to share with and inform other students of their experiences, as well as provide feedback to the instructors in question.
</p>

---

<a name="intro-scope"></a>
- 1.2 Scope

> - [Profiles](#intro_scope_profiles)
> - [Ratings](#intro_scope_ratings)

Here we will discuss the features we plan on covering in this or later versions of RCSP.

<a name="intro-scope-profiles"></a>
- 1.2.1 <i>Profiles</i>

<p>In general, profiles may be highly customizable web pages (which are necessarily open to inspection by RCSP staff to prevent inappropriateness) belonging to a single user. The medium through which high customizability is installed for each profile may be an interface which allows the writing of markdown and stylesheet code, which is dealt with accordingly by our processing and storage components, returning feedback to the user regarding the status of their input.</p>

<table>
  <tr>
    <td>FEATURE</td>
    <td>DESCRIPTION</td>
  </tr>

  <tr>
    <td>Student Profile</td>
    <td>
      <p>Students share a probably irrational fear that sharing their real identity on rating websites puts them in danger of receiving biased grades by professors in the loop.</p>

      <p>Our student profile feature will differ from the usual type to accommodate for this widespread belief; it is made impossible for one's profile to be referenced from one of their individual ratings until that rating has aged at least 6 months.</p>

      <p>Student profiles will consist of many of the usual details held in any typical user profile, along with references to ratings they've posted which are at least 6 months old.</p>
    </td>
  </tr>

  <tr>
    <td>Professor Profile</td>
    <td>
      <p>In keeping with our hopes for a communication hub to form between willing professors and students, a professor profile which may only be instantiated and therein useable by passing an authentication process will be implemented.</p>

      <p>From here professors may view relevant student ratings, find reference links to a location where they can easily interface with and respond to them, and report those ratings which upon inspection may happen to be inappropriate or unfair.</p>
    </td>
  </tr>
</table>

<a name="intro-scope-ratings"></a>
- 1.2.2 <i>Ratings</i>

<p>Every rating contains a template the rater must abide by, with potentially optional inputs. All ratings are first forwarded to the RCSP backend to evaluate appropriateness in terms of language. This technique can also help filter spam. Individual ratings will have the property of being "liked" or "disliked" by others, as well as commented on.</p>

<table>
  <tr>
    <td>FEATURE</td>
    <td>DESCRIPTION</td>
  </tr>

  <tr>
    <td>Professor Rating</td>
    <td>
      The key feature of RSCP is the professor rating. Student profiles may be allowed to comment on professors, with a template that goes over a wide range of aspects profiling the student's experience and feedback.
    </td>
  </tr>

  <tr>
    <td>Class Rating</td>
    <td>
      In some cases, a student may seek to focus on a particular class and the material covered rather than the professor. We allow for this, and so classes associated with their title and host institution will be viewable with respective ratings. A <i>class</i> and a <i>professor</i> do not inherently differ except that there is no such thing as a class profile. Raters may be optionally allowed to "forward" their class rating to the professor that taught it, effectively making the rating appear and exist in the record of both that class page and the professor's page.
    </td>
  </tr>

  <tr>
    <td>Student Rating</td>
    <td>
      At RCSP we do not bias against the professor, but at the same time recognize that it is not appropriate for a professor to publicly give negative comments to a student. So, professors are allowed to rate a student upon that student's private approval through the website, in which case the rating may be made either public or private by the student.
    </td>
  </tr>

  <tr>
    <td>Rating Likes & Dislikes
    <td>
      Every rating will come with a like/dislike button (or some other similar dichotomy) which other users can click on to compactly share their view on the rating.
    </td>
  </tr>

  <tr>
    <td>Rating Comments</td>
    <td>
      Any rating that has become public is open to comments from other users, including the rater. Comments share properties that ratings do: they can also be liked and disliked, and commented on, but nesting of comments will have an upper bound.
    </td>
  </tr>
</table>

---

<a name="intro-context"></a>
- 1.3 Context

<p>The current iteration of RCSP will be website based only. Plans for an Android application are not in the air, but part of the team is knowledgeable enough in the Android environment that such an idea is not far-fetched whatsoever.</p>
<p>For now, however, as much effort and development time as possible will be put into the website part of the product.</p>

---

<a name="intro-constraints"></a>
- 1.4 Constraints

<p>There are several constraints the development team will face.</p>
<p>For one, the team itself is not very large. At the time of writing 2 people are knowledgeable enough in web frameworks and languages necessary to at least get started on the product, but not to complete it.</p>
<p>As for knowledge, this is the (current) team's first web solution and so they still need to get acquainted with frameworks which'll make the code base more modular, as well as the possibly very many 'best practices' for web development and existing security protocols.</p>

---

<a name="use_cases"></a>
## 2. Use Cases
> - [Login](#uc-login)
> - [Create Account](#uc-create_account)

Here we follow a use case template to detail several different use cases within RCSP. The several use cases are described below, and we go into detail in their respective sections.

<table>
  <tr>
    <td>USE CASE</td>
    <td>DESCRIPTION</td>
  </tr>

  <tr>
    <td>Login</td>
    <td></td>
  </tr>

  <tr>
    <td>Create Account</td>
    <td></td>
  </tr>
</table>

---

<a name="uc-login"></a>
- 2.1 Login

<table>
  <tr>
    <td>FACTORS</td>
    <td>DESCRIPTION</td>
  </tr>

  <tr>
    <td>Actors</td>
    <td></td>
  </tr>

  <tr>
    <td>Priority</td>
    <td></td>
  </tr>

  <tr>
    <td>Precondition</td>
    <td></td>
  </tr>

  <tr>
    <td>User Interface</td>
    <td></td>
  </tr>

  <tr>
    <td>Scenarios</td>
    <td></td>
  </tr>
</table>

---

<a name="uc-create_account"></a>
- 2.2 Create Account

<table>
  <tr>
    <td>FACTORS</td>
    <td>DESCRIPTION</td>
  </tr>

  <tr>
    <td>Actors</td>
    <td></td>
  </tr>

  <tr>
    <td>Priority</td>
    <td></td>
  </tr>

  <tr>
    <td>Precondition</td>
    <td></td>
  </tr>

  <tr>
    <td>Postcondition</td>
    <td></td>
  </tr>

  <tr>
    <td>User Interface</td>
    <td></td>
  </tr>

  <tr>
    <td>Scenarios</td>
    <td></td>
  </tr>
</table>

---

<a name="design_overview"></a>
## 3. Design Overview
> - [Design Phases](#do-design_phases)
> - [Guiding Principles](#do-guiding_principles)
> - [Design Patterns](#do-design_patterns)
> - [Coding Style](#do-coding_style)

---

<a name="do-design_phases"></a>
- 3.1 Design Phases

---

<a name="do-guiding_principles"></a>
- 3.2 Guiding Principles

---

<a name="do-design_patterns"></a>
- 3.3 Design Patterns

---

<a name="do-coding_style"></a>
- 3.4 Coding Style

---

<a name="user_interface_design"></a>
## 4. User Interface Design
> - [Prototypes](#uid-prototypes)
> - [Justifications](#uid-justifications)
> - [Tradeoffs](#uid-perceived_tradeoffs)
> - [Discussion](#uid-discussion)

---

<a name="uid-prototypes"></a>
- 4.1 Prototypes

---

<a name="uid-justifications"></a>
- 4.2 Justifications

---

<a name="uid-perceived_tradeoffs"></a>
- 4.3 Tradeoffs

---

<a name="uid-discussion"></a>
- 4.4 Discussion

---

<a name="arch_and_comp_design"></a>
## 5. Architectural & Components Design
> - [MVC](#acd-mvc)
> - [Components](#acd-components)
> - [Hosts](#acd-hosts)
> - [Discussion](#acd-discussion)

---

<a name="acd-mvc"></a>
- 5.1 MVC

> - [Model](#acd-mvc-model)
> - [View](#acd-mvc-view)
> - [Controller](#acd-mvc-controller)

---

<a name="acd-mvc-model"></a>
- 5.1.1 <i>Model</i>

---

<a name="acd-mvc-view"></a>
- 5.1.2 <i>View</i>

---

<a name="acd-mvc-controller"></a>
- 5.1.3 <i>Controller</i>

---

<a name="acd-components"></a>
- 5.2 Components

---

<a name="acd-hosts"></a>
- 5.3 Hosts

---

<a name="acd-discussion"></a>
- 5.4 Discussion

---

<a name="data_model"></a>
## 6. Data Model
> - [Prototype Tables](#dm-prototype_tables)
> - [JSON Specification](#dm-json_spec)
> - [Database Specification](#dm-database_spec)
> - [Discussion](#dm-discussion)

---

<a name="dm-prototype_tables"></a>
- 6.1 Prototype Tables

---

<a name="dm-json_spec"></a>
- 6.2 JSON Specification

---

<a name="dm-database_spec"></a>
- 6.3 Database Specification

---

<a name="dm-discussion"></a>
- 6.4 Discussion

---

<a name="testing"></a>
## 7. Testing
> - [Protocols](#testing-protocols)

---

<a name="testing-protocols"></a>
- 7.1 Protocols

---

<a name="appendices"></a>
## 8. Appendices
> - [Definitions](#appendices-definitions)
> - [Errata](#appendices-errata)
> - [Revision History](#appendices-revision_history)

---

<a name="appendices-definitions"></a>
- 8.1 Definitions

---

<a name="appendices-errata"></a>
- 8.2 Errata

---

<a name="appendices-revision_history"></a>
- 8.3 Revision History

<p>
Note that all revisions are tracked once Version 1.0 of the documentation is released.
</p>


[RCSP_Repo]: https://github.com/ModuKai/RateMyCSProfessor "Rate My CS Professor Repository"
