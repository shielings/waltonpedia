# Waltonpedia

## A wiki for neurology doctors at The Walton Centre

![alt-text](screenshot2.png?raw=true)


### What is this?
This is a proposed trial use of a wiki to gather and serve the information needed for doctors at The Walton Centre to get work done, similar to a junior doctor's handbook.

### Why?
Doctors working in neurology require information and guidance on many clinical and administrative tasks. Neurological tests, treatments and procedures can be complicated to organise because they involve external hospitals and labs. The methods often change and can be hard to keep track of. The information required to manage these is split between the traditional means of clinical handover - intranet, emails, pinboards and word-of-mouth. Other information, including teaching schedules, specialist rotas and clinic guides is also distributed using these varying means. It can be daunting for a new junior doctor to assimilate all of this information.

### Our solution
A [wiki](https://en.wikipedia.org/wiki/Wiki) is a website that can be edited by its users. It can be hosted on the open internet with certain privileges (editing or viewing sensitive information) being locked behind a login requiring a Walton Centre email address. We propose such a wiki, hosted and used by the medical staff. This will make it easier to disseminate, update and find information.

### What makes this better than the intranet, emails etc...?
![alt-text](Picture2.png?raw=true)
- Rapid access access from anywhere with internet, on any device with a web browser using a short, memorable URL - [walton.wiki](https://walton.wiki)
- (Mostly) Open - public access for non-sensitive data
- Editable by any Walton Centre staff willing to make improvements
- Consistent - no more "old PDFs" found in emails
- Highly auditable - every update to every page is kept and labelled with the author's name. Recent changes are highlighted for scrutiny by other editors.
- User-centric design

|                     |  Intranet | Emails | Pinboards  | Word-of-mouth | Waltonpedia |
|---------------------|:---------:|:------:|:----------:|:--------------:|:-----------:|
| Ease of access      | ❌        | ✅   | ❌         | ❌            | ✅           |              
| Ease of updating    | ❌        | ✅   | ✅         | ✅            | ✅           |
| Accuracy            | ❌        | ❌   | ❌         | ✅            | ✅           |
| Relevance           | ❌        | ✅   | ✅         | ✅            | ✅           |
| Clinical governance | ✅        | ❌   | ❌         | ❌            | ✅           |
| Audit trail         | ❌        | ✅   | ❌         | ❌            | ✅           |

### To-do
✅Access from the private domain name [walton.wiki](walton.wiki)

✅Email server for secure user registration and password resets

✅Permissive robots.txt

⬜Analytics server with public access to usage data

### Caveats and clinical governance

- This wiki will not hold any patient identifying data at all. It's primary purpose is administrative help. It can therefore be hosted outside of the NHS.
- There should be training and regular reminders to staff to understand that this is the equivalent of a printed junior doctors handbook written by their peers. It does not constitute official Walton Centre policies and procedures, which must be consulted separately
- This is not a replacement for any of the previous ways of passing on information. They will all work together. For example, the intranet should still be used to access a formal guideline, but you may need to ask someone verbally how to find it. You may need an email to remind you to sign up for a grand round slot on the wiki. You might use the wiki to quickly look up a radiologist's phone number whilst organising a thrombectomy.
- New and updated content will be reviewed by other editors to ensure it is accurate and clear
- Senior approval will be sought for every change to this service

### Proposed next steps
`August 2022` Discuss with seniors to see if a limited trial can be started. Start with interested neurology registrars.

`November 2022` Open up access to selected SHOs with a training session on what Waltonpedia is (and isn't!)

`February 2023` Open up to all Walton neurology SHOs and neurology registrars

`July 2023` Assess impact formally and see if the service is worth continuing

`Later` Provide content for neurology medical students, consultants and also junior doctors at referring hospitals.

### How can I recreate this?
In case of a problem with Waltonpedia or staff changes, the system can be recreated with the following steps:
- Clone this repository
- Copy the Bookstack data (synchronised to the following people's computers....any volunteers?) to /bookstack
- Install Docker and docker-compose on a compatible system. I used Ubuntu Server 22.04 on a Dell Poweredge T20 where the command is `sudo apt install docker.io docker-compose`
- cd into the /waltonpedia folder and run the docker-compose file with the command `sudo docker-compose up -d`
- This will create docker containers for SWAG, Bookstack and mariaDB
- Point the domain name [walton.wiki](https://walton.wiki) (in joint ownership between the following people...) to your public ip with ports 80 and 443 forwarded to your server

### Acknowledgements

Thank you to the contributors of Bookstack, linuxserver.io for SWAG, LetsEncrypt
