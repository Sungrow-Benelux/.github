# Sungrow Benelux EV charging - software development guide (github:octocat:)

## Team members
:eyes: (High quality pictures/drawing for the team members required here) :eyes: \
:sun_with_face::sun_with_face:
| Member | Responsibility |
|--| -- |
|:sunglasses: Jingzhe Liang  | :clipboard:|
|:sunglasses: Qi Yu  | :clipboard:  |
|:sunglasses: Qihao Xia  | :clipboard:  |
|:sunglasses: Qixiang Xu   | :clipboard:|
|:sunglasses: Shengqing Ma  | :clipboard:  |
|:sunglasses: Winer Bao  | :clipboard:  |
|:sunglasses: Xiaoyao Luo   | :clipboard:  |
|:sunglasses: Yu Ni  | :clipboard:  

## Useful tools

:space_invader: Here, we list some useful tools for the software development. If you have more secret weapons, feel free to add them!
### Github tools
#### [gitk](https://git-scm.com/docs/gitk/)
It is a powerful UI to indicate the commit history and branches in git. Use it on the command line to track the commit history.
it can be easily installed via 
```bash
sudo apt-get install gitk
```
#### [conventional changelog](https://github.com/conventional-changelog/conventional-changelog)
It is a helpful tool to align your commit message with the angular rules. If you commit your code following this tool's instruction everytime, 
the generation of the changelog will be fully automated, via a simple command. To config the application, refer to: [conventional changelog config](https://www.npmjs.com/package/conventional-changelog-custom-config).\
Here is an example for the changelog:
![Screenshot from 2022-12-28 15-11-49](https://user-images.githubusercontent.com/65727493/209824976-f0f879a2-59e7-488b-9c1a-203bceb7221c.png)
#### [git flow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
git flow is a tool for the branching model, which can standardlize the repo release cycle. It assigns very specific roles to different branches and defines how and when they should interact. Check the link for more introduction, and the developers should follow this branching model one way or the other. The config file for the git flow should be aligned to:
```bash
[gitflow "branch"]
	master = main
	develop = dev
[gitflow "prefix"]
	feature = feat
	bugfix = fix
	release = release
	hotfix = hotfix
	support = support/
	versiontag = 
[gitflow "path"]
	hooks = /path/to/projects/.git/hooks
```

By using 
```bash
git flow init
```

The command will guide you to setup all the branches's default prefix. The config file will be located in /.gits/config, double-check the content or use:
```bash
git flow config
```
to verify the settings.

### Documentation
#### [Doxygen](https://www.doxygen.nl/)
It is a generally used code documentation generation tool. Development packages that we use, like Qt, ST, their source codes are all documented following the doxygen style.
If you want to document the class, functions, members, variables, or the entire code project, and generate a hyper-link based HTML wiki, make sure you
document them in a doxygen way, and generate the docs using the application.

#### [Plantuml](https://plantuml.com/)
Plantuml is not doubt the most powerful tool to generate the UML design diagrams, or even salt diagram, WBS and structured JSON documents. It generates the diagram
via the interpreted language, and it is easy to understand (except the activity diagram, dont use it until it luckily gets better in the future). \
In our team, we nearly over-abuse it to generate the **class diagrams, sequence diagrams, components diagrams or states' diagram**. They are helpful for the 
discussion, review, debugging and documentation.

#### [Visual paradiagm](https://www.visual-paradigm.com/)
If you want more fancy and customisable diagrams, visual paradiagm could be a good choice. Sometimes, if we want to draw some fancy block diagrams, state diagrams for the
presentation to indicate that we are doing a great job, we will use it, with gratitude.

#### [diagrams.net](https://www.diagrams.net/)
Diagrams.net is a drawing tool similar to the visual paradiagm. Its main strength is, the edited diagrams' source file can be store locally, and its overall style is more clean and simple.
It can be used as an alternative choice for visual paradiagm.

#### [ReText](https://github.com/retext-project/retext), [Ghostwriter](https://ghostwriter.kde.org/)
When dealing with github, we will have to write many markdown style files. In our daily job, markdown style writing is also a quick way to take notes,
write a technical documents for the codes, or just simply write some random texts that could help you think. ReText and Ghostwriter are both markdown
style text writing tools. Considering the colorful markdown parsing style in different tools, it will be good to have both.

#### [sublime text](https://www.sublimetext.com/docs/linux_repositories.html#apt)

#### [Overleaf](https://www.overleaf.com/)
A de facto standard online edit tools for the Latex writing. Using the latex document's template, you can write a fancy and well-structured instruction manual, 
a test report, a specification document, a design report, or a application for a better technical solution. Presenting the documents written in latex with overleaf
is like wearing a formal suit, sometimes you have to wear it when you are dealing with important people.

### Coding standard (still working on it)
#### Google C++ open-source coding style
#### Sungrow C Coding standard
#### Valgrind
#### PC-lint
