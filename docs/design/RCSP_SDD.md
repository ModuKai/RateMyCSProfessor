# [Rate My CS Professor][RCSP-Repo]

## Software Design Documentation
##### Version: 1.0
##### Date: 04-19-2016

---

## Table of Contents
> 1. [Introduction](#introduction)
> 2. [Use Cases](#use-cases)
> 3. [Design Overview](#design-overview)
> 4. [User Interface Design](#user-interface-design)
> 5. [Architectural & Components Design](#arch-and-comp-design)
> 6. [Data Model](#data-model)
> 7. [Testing](#testing)
> 8. [Appendices](#appendices)

---

<a name="introduction"></a>
## 1. Introduction
> - [Goals & Objectives](#intro_goals-and-objectives)
> - [Scope](#intro_scope)
> - [Context](#intro_context)
> - [Constraints](#intro_constraints)

<p>
  The purpose of this software design document is to outline and carefully describe different aspects of the [RateMyCSProfessor][RCSP-Repo] website through a developmental lens, primarily for developmental purposes. However it may also be used as not only a primer for anyone newly involved in the project, but as an updated reference to the current design model. Any API-related investigations are irrelevant here.
</p>
<p>
  Design decisions may change, and so there will consequently occur changes & updates to this document at any given time, with a revision history kept.
</p>

---

<a name="intro_goals-and-objectives"></a>
- 1.1 Goals & Objectives

<p>
  The [RateMyCSProfessor][RCSP-Repo] website is meant to be a domain-specific rating & feedback website in which both students and instructors may participate.
</p>
<p>
  It differs from other instructor rating websites in that it allows a rater to go more in depth regarding his or her experience with the instructor, by virtue of domain-specificity. Whereas other websites are tailored to a general audience, where the rating template is too simplistic and often gives very limited useful information to curious students, a domain-specific rating website is specially capable of allowing a larger amount of relevant data to be inputted in a sensible way and consequently shared with students searching for exactly that type of detailed information.
</p>
<p>
  We hope to build a rating template that serves raters easily and, most importantly, as fully as possible. Students read other students ratings, and hopefully benefit from each other when a reader becomes a rater. In this way a community of raters begins to form.
</p>
<p>
  One fundamental aspect of the instructor rating environment is that the instructor is not necessarily left out. In [RateMyCSProfessor][RCSP-Repo], willing instructors will be provided the means to communicate with raters of their choosing. What essentially happens is there begins to form an organized way for instructors to receive feedback from students as well as respond to that feedback publically.
</p>
<p>
  [RateMyCSProfessor][RCSP-Repo], in this way, becomes a communication board between instructors looking to improve and refine their teaching skills and standards, and students wanting to share with and inform other students of their experiences, as well as provide feedback to the instructors in question.
</p>

---

<a name="intro_scope"></a>
- 1.2 Scope
> - [Profiles](#intro_scope_profiles)
> - [Ratings](#intro_scope_ratings)

Here we will discuss the features we plan on covering in this or later versions of [RCSP][RCSP-Repo].

---

<a name="intro_scope_profiles"></a>
- 1.2.1 <i>Profiles</i>

<p>In general, profiles may be highly customizable pages (which are also open to inspection by [RCSP][RCSP-Repo] staff to prevent inappropriateness) belonging to a single user. The medium through which customizability is installed into each profile may be an interface which allows the writing of markdown and stylesheet code, which is dealt with accordingly, returning feedback to the user regarding the status of their input.</p>

<table>
  <tr>
    <td>FEATURE</td>
    <td>DESCRIPTION</td>
  </tr>

  <tr>
    <td>Student Profile</td>
    <td>
      <p>Students share a probably irrational fear that sharing their real identity on rating websites puts them in danger of receiving biased grades by the same or other professors.</p>

      <p>Our student profile feature will differ from the usual type to accomodate this widespread belief so that it is impossible for one's profile to be referenced from one of their individual ratings until that rating has aged at least 6 months.</p>

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

---

<a name="intro_scope_ratings"></a>
- 1.2.2 <i>Ratings</i>

<table>
  <tr>
    <td>FEATURE</td>
    <td>DESCRIPTION</td>
  </tr>

  <tr>
    <td>Professor Rating</td>
    <td>

    </td>
  </tr>

  <tr>
    <td>Class Rating</td>
    <td>

    </td>
  </tr>

  <tr>
    <td>Student Rating</td>
    <td>

    </td>
  </tr>
</table>

---

<a name="intro_context"></a>
- 1.3 Context

---

<a name="intro_constraints"></a>
- 1.4 Constraints

---

<a name="use-cases"></a>
## 2. Use Cases
> - [Actors](#uc_actors)

<a name="uc_actors"></a>
- 1.1 Actors

---

<a name="design-overview"></a>
## 3. Design Overview
> - [Design Phases](#do_design-phases)
> - [Guiding Principles](#do_guiding-principles)
> - [Design Patterns](#do_design-patterns)
> - [Coding Style](#do_coding-style)

---

<a name="do_design-phases"></a>
- 3.1 Design Phases

---

<a name="do_guiding-principles"></a>
- 3.2 Guiding Principles

---

<a name="do_design-patterns"></a>
- 3.3 Design Patterns

---

<a name="do_coding-style"></a>
- 3.4 Coding Style

---

<a name="user-interface-design"></a>
## 4. User Interface Design
> - [Prototypes](#uid_prototypes)
> - [Justifications](#uid_justifications)
> - [Tradeoffs](#uid_perceived-tradeoffs)
> - [Discussion](#uid_discussion)

---

<a name="uid_prototypes"></a>
- 4.1 Prototypes

---

<a name="uid_justifications"></a>
- 4.2 Justifications

---

<a name="uid_perceived-tradeoffs"></a>
- 4.3 Tradeoffs

---

<a name="uid_discussion"></a>
- 4.4 Discussion

---

<a name="arch-and-comp-design"></a>
## 5. Architectural & Components Design
> - [MVC](#acd_mvc)
> - [Components](#acd_components)
> - [Hosts](#acd_hosts)
> - [Discussion](#acd_discussion)

---

<a name="acd_mvc"></a>
- 5.1 MVC

> - [Model](#acd_mvc_model)
> - [View](#acd_mvc_view)
> - [Controller](#acd_mvc_controller)

---

<a name="acd_mvc_model"></a>
- 5.1.1 <i>Model</i>

---

<a name="acd_mvc_view"></a>
- 5.1.2 <i>View</i>

---

<a name="acd_mvc_controller"></a>
- 5.1.3 <i>Controller</i>

---

<a name="acd_components"></a>
- 5.2 Components

---

<a name="acd_hosts"></a>
- 5.3 Hosts

---

<a name="acd_discussion"></a>
- 5.4 Discussion

---

<a name="data-model"></a>
## 6. Data Model
> - [Prototype Tables](#dm_prototype-tables)
> - [JSON Specification](#dm_json-spec)
> - [Database Specification](#dm_database-spec)
> - [Discussion](#dm_discussion)

---

<a name="dm_prototype-tables"></a>
- 6.1 Prototype Tables

---

<a name="dm_json-spec"></a>
- 6.2 JSON Specification

---

<a name="dm_database-spec"></a>
- 6.3 Database Specification

---

<a name="dm_discussion"></a>
- 6.4 Discussion

---

<a name="testing"></a>
## 7. Testing
> - [Protocols](#testing_protocols)

---

<a name="testing_protocols"></a>
- 7.1 Protocols

---

<a name="appendices"></a>
## 8. Appendices
> - [Definitions](#appendices_definitions)
> - [Errata](#appendices_errata)

---

<a name="appendices_definitions"></a>
- 8.1 Definitions

---

<a name="appendices_errata"></a>
- 8.2 Errata


[RCSP-Repo]: https://github.com/ModuKai/RateMyCSProfessor "Rate My CS Professor Repository"
