# Notes on FAC19 workshops weeks 1-8

# Week 1

## Accessability

- can you access everything via keyboard only?
- don't rely on colour alone to convey info.
- use a contrast checker to test for colour contrast.

#### Chrome Extensions:
- HTML5 outliner 
- ChromeVox  (close your eyes, listen, navigate with keyboard only)
(disable voice by clicking ```ctrl``` or disable altogether with ```ctrl + alt + z```)
- Accessability Dev Tools (allows to run audit in dev tools)

## Design Burst
- use HSL instead of RGB
- True grey has 0% saturation

## CSS variables
- Look at Refactoring UI book
- Can use a checkbox input to toggle on or off (in js) a css class on a DOM element (e.g. to change the colour theme). (Can use css and divs to design the checkbox in a slider fashion). (See workshop code for details).

## Git Workflow
- Ref: https://guides.github.com/introduction/flow/
- (With GitHub, you can deploy from a branch for final testing in production before merging to master.

Once your pull request has been reviewed and the branch passes your tests, you can deploy your changes to verify them in production. If your branch causes issues, you can roll it back by deploying the existing master into production.)

- git fetch --all (pulls all remote branches?)
git checkout branch-name 
- (can see branches visually as well in github).
git log --oneline --decorate --graph --all

- WORKFLOW
0) go to folder which you want to clone the file to 
~cd doc
1) git clone url       (copies from remote)
2) cd folder_name (go inside the folder you cloned)
3) git checkout -b branch-name  (makes a new branch and goes into it?)
4) git status (See which files have been changed)
5) git add
6) git commit -m "descriptive message
Relates #1"  (relates to issue 1) 
7) git checkout master
8) git pull    (pulls the master into local)
9) git checkout branch-name
7-9) shortcut:   git pull origin master
10) git merge master
git add, git commit, (if there are merge conflicts which you change).
11) git push origin branch-name       (never push to master)
12) then can create pull request on gitHub    (to update Master with your branch)
13) git checkout master
(can delete branch after it has been accepted into pull request .....unless you want to keep working with that feature/branch name).

## HTML Forms
- different input types. (textarea, type="email", "phone", "checkbox", "radio", "text",...)
- button default behaviour in a form type="submit" (good to explicitly add this to form button)
- When submitted, a form will send a GET request to the URL in its action attribute. This can be a relative URL within the same site (/submit) or an external URL to some other API (https://some-other-api.com/submit).
- All inputs with a name attribute within your form will be submitted. By default they'll be sent as the "search" part of the URL (often called the querystring; it's the bit following a "?"). It will be structured like "url.com?name=value&otherInput=otherValue", with each name/value pair separated by an ampersand (&).
    Some input types submit differently. For example a checkbox's value will either not be present (unchecked) or will be the input's value attribute (checkboxName=checkboxValue). If you don't set a value it will default to "on" (checkboxName=on). Groups of radios with the same name should have value attributes, which is what they will submit (radioGroupName=selectedValue).

-- FINISH WORKSHOP EXERCISES

# Week 2


# Week [SOMEHTH9NG] - Node

- nodemon 
- modules: fs, path, url
- go over difference between 'require' and 'import'
- module.exports.
- router -- how to build properly in vanilla node
- npm --- how to use version manager of dependencies properly. how to check for security risks. how to find reliable packages. 

# Week 6 - Authentication

### Cookies
- cookies stored on the browser are specific to the domain. 
- cookies can be attached to the response from a server, in the header, 'Set-Cookie'. 
- In Node.js, res.setHeader is used for setting single headers, res.writeHead can be used for setting multiple headers at the same time.
```javascript
res.setHeader('Set-Cookie', 'logged_in=true');

// OR

res.writeHead(200, { 'Set-Cookie': 'logged_in=true' });
```
- ```req.headers.cookie``` is used to read the cookie sent by the server 
- its easy to change cookies in the client so it is not secure and can be tampered with, unless you protect it in some way (see later workshop)
- add (flags)[https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Set-Cookie] to cookie to make it more secure. e.g. ```res.setHeader('Set-Cookie', 'logged_in=true; HttpOnly; secure; Max-Age=9000');```. ```secure``` can only be used with https requests. HttpOnly prevents JS being inserted (ie XSS attack). Max-age sets life time of cookie in seconds.
- can delete a cookie by overwriting it or setting max-age to 0. 
- **3rd party cookies**. a site (say foo.com) will not send cookies to another server (say bar.com). but bar.com can access cookies from foo.com, through javascript (by making an AJAX request). hence if you're on a page with some 3rd party javascript running, e.g. a facebook comment box for example, even if you're not on the facebook site, it can track you independently of the domain you're on. Some browsers allow you to turn off 3rd party cookies. 

#### Questions
- I seem to be able to set a cookie using a GET request as well as a POST request, but for some reason, when i change the method on the html form to GET, with action='login', and click submit, it redirects to 'index.html/login?' instead of 'index.html/login'. Why 
does the question mark appear when its a get request?... i.e. is it because a forms default behaviour to always send a query string paramater, even if it is empty? does a form always expect to send a post request
and so sending a get request from a form is wrong?
is it possible to change this default behaviour? 
- Is it normal to set cookies only on post request? or can it also be set on a get request?
- Whats the difference between cookies and using local/session storage? Are cookies only available in browsers (but not other clients such as native apps)?
- Aside: how do native apps make requests to the server (as fetch() is a browser method right?)
- what is typeof req.headers.cookie? 
- why do the console logs come up in the terminal instead of the browser when logging from the router?
- when deleting a cookie is it also important to set the HttpOnly? 
- what happens if you leave out res.end()?
- what is the value in setting the Content-Length header?

#### Look up
- readFile
- module.exports
- __dirname
- why use path.join? why not just store in an array and use .join()?
- how does one error handle on line 13 of router.js
- go over different response codes. how is client behaviour (in particular browsers) affected by the different response codes sent? what if you send the wrong response code?
- use cases of cookies in production level code. and alternatives to cookies.