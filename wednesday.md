# 99 ways to kill your open source project
- OS Guy from github Brandon Keepers
 - Free as in puppies
  - fun when young and cutes
  - ruin everything but its not their fault
## Kill the Motivation of Maintainers
  - avoid giving constructive feedback
  - don't read contributing guidelines
  - make contributions difficult to accept
## Ruin the confidence of Users
  - vague description
  - no readme
  - if there is readme doesn't tell you how to use the thing
  - make releases unreliable irregular and infrequently
  - avoid roadmaps ("be agile")
## Ruin code integrity
  - inappropriate license
  - depend on many trivial libraries
  - accept all the pull requests
## Ruin the community
  - poorly manage community contributions
  - spend all your energy feeding the trolls


# Type Google into your Browser What Happens Next
- Graeme Mathieson @mathie
- http < first we check the cache
  - next: look at expires and other cache header to see if we need to reprime cache
- now we parse scheme http/https hostname=google.com aka authority maybe a port as well
- next we do dns lookup hit os resolver for ip
- name service switch to do local or localish lookups for dns so we don't have to always hit remote servers
- and a half second later, we can now make a TCP connection


# NEO4j Graph Database
- Relational Databases vs Graph
  - Joins are the main data, its all about the relationships
- SQL all the way up and down is current in indursty but doesn't solve al lproblems well
- When you just watched a bugs life you don't want 'The human centipede'

# CoreOS Essentials in Debian
- Docker is the new hotness this year, being rolled out all over
  - this + kubernetes isn't only possible future
- Wanted to insert coreos into debian
- etcd important for container communication and registration
- systemd necessary to make all this work
