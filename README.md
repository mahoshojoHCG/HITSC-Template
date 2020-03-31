# HITSC-Template

A Templete with Gradle and CI!

## How to use it

``` shell
git clone https://github.com/mahoshojoHCG/HITSC-Template.git
git remote set-url $(YOUR_LAB_REPOSITORY_ADDRESS)
git remote -v
#verify if your remote has changed.
git push -u origin master
```

Everything will work automantic after you push.

**Don't forget to add source to `sourceSets` in `build.gradle` if you have more or less labs.**
