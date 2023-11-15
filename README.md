# Gruyere
Google Gruyere's vulnerable webapp

## Running Gruyere locally

WARNING: Because Gruyere is very vulnerable, it includes some protection against being exploited by an external attacker when run locally. You'll see these parts of the code marked DO NOT CHANGE. Gruyere only accepts requests from localhost and uses a random unique id in the URL. However, it's difficult to fully protect against an external attack. And if you make changes to Gruyere you could make it more vulnerable to a real attack. Therefore, you should close other web pages while running Gruyere locally and you should make sure that no other user is logged in to the machine you are using. 

To run Gruyere locally, you'll first need to install Python 2.7, if you don't already have it. Gruyere was developed and tested with version 2.7 and may not work with other versions of Python. Download Gruyere itself from https://google-gruyere.appspot.com/gruyere-code.zip and unpack it to your local disk. Then to run the application, simply type:

``` $ cd <gruyere-directory> ```

``` $ ./gruyere.py ```


---

## Gruyere's Structure

- ```gruyere.py``` the main Gruyere web server
- ```data.py``` stores the default data in the database. There is an administrator account and two default users.
- ```gtl.py``` the Gruyere template language
- ```sanitize.py``` the Gruyere module used for sanitizing HTML to protect the application from security holes.
- ```resources/...``` holds all template files, images, CSS, etc.

---

## Gruyere's Features

- HTML in Snippets: Users can include a limited subset of HTML in their snippets.
- File upload: Users can upload files to the server, e.g., to include pictures in their snippets.
- Web administration: System administrators can manage the system using a web interface.
- New accounts: Users can create their own accounts.
- Template language: Gruyere Template Language(GTL) is a new language that makes writing web pages easy as the templates connect directly to the database. Documentation for GTL can be found in gruyere/gtl.py. 

---


## Threat Diagram

![gruyereThreatDiagram](https://github.com/KintsugiCode/gruyere/assets/41804800/ecf557da-2f78-4b2a-a3d4-22de115db399)


---


## Threat Model

#### Cybersecurity measures implemented can be found in the open PRs and are elaborated on in the following threat model document

https://docs.google.com/document/d/e/2PACX-1vSl7NHOCI8WmsNo4y_KhtT34-lDKWox5i_PLhvRdVqVteUqsiXTZcU4AIZMzBF5dem2XBVNpOeW54tX/pub

