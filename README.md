# DNS-Domain-Name-System-

## What is DNS?
DNS (Domain Name System) is like the phonebook of the internet.

Humans access websites using names like www.google.com.

Computers access websites using IP addresses like 142.250.190.36.

DNS translates domain names into IP addresses, so browsers can load internet resources.

### Why Do We Need DNS?
Imagine if you had to remember the IP address of every website you wanted to visit—just like memorizing phone numbers. DNS makes it easy by letting you use easy-to-remember names.

#### For example:

You type: www.facebook.com

DNS finds the IP address of Facebook’s server.

Your browser connects to that IP and loads the site.

## How DNS Works – Step by Step
Let's say you want to visit www.example.com.

#### 1. User Types the Domain Name
You enter www.example.com in your browser.

#### 2. Browser Checks Local Cache
Your browser first checks if it already knows the IP address. If yes, it skips DNS and loads the page.

#### 3. Operating System DNS Cache
If the browser doesn’t know, it asks the OS. The OS checks its own cache.

#### 4. Query Sent to DNS Resolver (Recursive Resolver)
If not in the cache, the request is sent to a recursive DNS resolver, usually run by your ISP (like PTCL, Comcast, etc.).

#### 5. Recursive Resolver Contacts Root DNS Server
The resolver asks the Root DNS Server: “Where can I find .com domains?”

The root server responds with the address of the TLD server for .com.

####  6. Resolver Contacts TLD Server
Now it asks the Top-Level Domain (TLD) server for .com: “Where is example.com?”

TLD server responds with the authoritative DNS server for example.com.

#### 7. Resolver Contacts Authoritative DNS Server
Finally, it asks the authoritative server: “What is the IP for www.example.com?”

The authoritative server responds with the IP, like 93.184.216.34.

#### 8. Resolver Returns IP to Your Browser
The resolver gives the IP address to your browser.

#### 9. Browser Connects to the Website
The browser connects to the IP address and loads www.example.com.

## DNS Caching
To speed things up, DNS information is cached at multiple levels:

Browser cache

Operating System cache

ISP DNS resolver cache

This prevents repeating the full process every time.
