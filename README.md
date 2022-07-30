# Waltonpedia

## A wiki for neurology doctors at The Walton Centre

![alt-text](https://raw.githubusercontent.com/shielings/waltonpedia/main/screenshot2.png?token=GHSAT0AAAAAABW4MREC5VXXE442LF7EO7QEYXFAKCA)

### Why?
Clinical neurology requires many different tests, treatments and procedures. These can be complicated to organise because they involve outside hospitals and labs. The methods often change and can be hard to keep track of. The information required to manage these is split between the traditional means of clinical handover - intranet, emails, pinboards and word-of-mouth. It can be daunting for a new junior doctor to assimilate all of this information.

### Our solution
A [wiki](https://en.wikipedia.org/wiki/Wiki) is a website that can be edited by its users. It can be hosted on the open internet with certain privileges (editing or viewing sensitive information) being locked behind a login requiring a Walton Centre email address.

### What makes this better than the intranet, emails etc...?
- Rapid access - a memorable URL and public access for non-sensitive data
- Editable by any Walton Centre staff willing to make improvements
- Pervasive (access from anywhere with internet, on any device with a web browser)
- Consistent - no more "this is an old PDF" found in an email
- Highly auditable - every update to every page is kept and labelled with the author's name
- Enjoyable to use which retains a sparkle of our personalities!

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

### How can I recreate this?
In case of a problem with Waltonpedia or staff changes, the system can be recreated with the following steps:
- Clone this repository
- Copy the Bookstack data (synchronised to the following people's computers....MBO?) to /bookstack
- Install Docker and docker-compose on a compatible system. I used Ubuntu Server 22.04 on a Dell Poweredge T20 where the command is `sudo apt install docker.io docker-compose`
- cd into the /waltonpedia folder and run the docker-compose file with the command `sudo docker-compose up -d`
- This will create docker containers for SWAG, Bookstack and mariaDB
- Point the domain name [walton.wiki](walton.wiki) (in joint ownership between the following people...) to your public ip with ports 80 and 443 forwarded to your server

### Acknowledgements

Thank you to the contributors of Bookstack, linuxserver.io for SWAG, LetsEncrypt
