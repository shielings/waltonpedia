# Waltonpedia

## A wiki for doctors working at The Walton Centre

### Why?
The information needed to work at this hospital was previously fragmeneted between the intranet, emails, induction paperwork, posters and word-of mouth. This project aims to bridge these means to provide a rapid, accurate source of information.

### What makes this better than the intranet, emails etc...?
- Rapid access - a memorable URL and public access for non-sensitive data
- Enjoyable to use - with a sparkle of our personalities!
- Editable by those willing to make improvements
- Pervasive and consistent - no "this is an old PDF" found in an email
- Highly auditable - every update to every page is kept and labelled with the author's name

### To-do
- [x]Login from a private domain
- [ ]Email server for user registration and password resets
- [ ]Analytics server with public access to usage data

### How can I recreate this?
In case of a problem with Waltonpedia or staff changes, the system can be recreated with the following steps:
- Install Docker and docker-compose on a compatible system. I used Ubuntu Server 22.04 on a Dell Poweredge T20
- Clone into this repository and run the docker-compose file with the command `sudo docker-compose up -d`
- This will create docker containers for 
-- SWAG (reverse proxy with SSL certifcates
-- 

### Acknowledgements

Thank you to the contributors of Bookstack, linuxserver.io for SWAG, LetsEncrypt
