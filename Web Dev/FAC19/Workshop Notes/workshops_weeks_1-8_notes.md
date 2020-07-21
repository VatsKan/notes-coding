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

