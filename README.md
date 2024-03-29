---
Title: My Personal Website
tags: Templates, DevOps
description: Mon CV "Slide Mode".
Authors: Laurent Marques
---

# My Personal Website

<!-- Put the link to this slide here so people can follow -->

To render your Markdown-based slideshow on the fly, checkout [Remarkise](https://gnab.github.io/remark/remarkise).

slide: https://hackmd.io/@metalfrags/S1BX7J5aH

---


Template website CV Revision: 0.0.1

Please prepare laptop or smartphone to join this community!

---

## Who am I?
Hi my name is Laurent,

I from in France, i love technologies, informatique and computeur, programming... and very best challenge.
For my work i use more technologies.

And you, how are you ?

I suggest you get to know me below :8ball: 

---

### My Background

- Hardware computer Technician
- Network Administrator
- Front-end developper Junior, 
- Solution Architecte 
- Ingénieur Cloud DevOps

---
### Tools and OS i use :100: 
- VSCode, Pycharm
- Linux, Mac Os, Windows, 
- Emacs, Vim, HackMD and AWS :heart: 

---


### Langage: 

- Python3, Bash, MD, HTML, Css, yaml, json
    - I love Github and Gitlab for versionning with  Hack MD for create best project :+1: 
- I use tabs. :cat: 

---

### Actually Mission:
- Gekko (Team Support Airbus)
 >With Airbus SAS to create the best projects :+1:
- Team support is the best !
- Onboarding process

---

### Consulting
>And DevOps Teachers for Gekko Academy

---

### Onboarding Process
- Agiles methods, Scrum, Kanban (Jira Admin, Confluence, Trello) 
    - Onboarding Process (Tools DevOps)
- Team Leader
    - curious, dynamic, best effort, 
- Owner, Admin, Organisation Versionning (Github, Gitlab)
- Mode Project
- Best practice

---

### Deploy 
- Architecturing your application in the AWS Cloud
- DevOps (CI/CD)
- Ansible, Terraform, Cloud formation
- Artifactory 
- Best practice

---

### 70% of our users are developers. Developers :heart: GitHub.

---

{%youtube E8Nj7RwXf0s %}

---

### Usage flow

---


```graphviz
digraph {
  compound=true
  rankdir=RL

  graph [ fontname="Source Sans Pro", fontsize=20 ];
  node [ fontname="Source Sans Pro", fontsize=18];
  edge [ fontname="Source Sans Pro", fontsize=12 ];


  subgraph core {
    c [label="Hackmd-it \ncore"] [shape=box]
  }
  
  c -> sync [ltail=session lhead=session]

  subgraph cluster1 {
     concentrate=true
    a [label="Text source\nGithub, Gitlab, ..."] [shape=box]
    b [label="HackMD Editor"] [shape=box]
    sync [label="sync" shape=plaintext ]
    b -> sync  [dir="both"]
    sync -> a [dir="both"]
    label="An edit session"
  }
}
```

---

### Architecture of extension

---

![](https://i.imgur.com/ij69tPh.png)

---

## Content script

- Bind with each page
- Manipulate DOM
- Add event listeners
- Isolated JavaScript environment
  - It doesn't break things

---

# :fork_and_knife: 

---

<style>
code.blue {
  color: #337AB7 !important;
}
code.orange {
  color: #F7A004 !important;
}
</style>

- <code class="orange">onMessage('event')</code>: Register event listener
- <code class="blue">sendMessage('event')</code>: Trigger event

---

# :bulb: 

---

- Dead simple API
- Only cares about application logic

---

```typescript
import * as Channeru from 'channeru'

// setup channel in different page environment, once
const channel = Channeru.create()
```

---

```typescript
// in background script
const fakeLogin = async () => true

channel.answer('isLogin', async () => {
  return await fakeLogin()
})
```

<br>

```typescript
// in inject script
const isLogin = await channel.callBackground('isLogin')
console.log(isLogin) //-> true
```

---

# :100: :muscle: :tada:

---

### Wrap up

- Cross envornment commnication
- A small library to solve messaging pain
- TypeScript Rocks :tada: 

---

### Thank you! :sheep: 

You can find me on

- GitHub
- Twitter
- or email me

![Gekko](https://github.com/Les-Geeks/Documentation/blob/dev/img/LOGO_GEKKO_LES-INGENIEURS-DU-CLOUD_RVB-1_import.png)
