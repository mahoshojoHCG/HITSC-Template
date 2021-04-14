# HITSC-Template

A Templete with Gradle and CI!

[**简体中文**](https://github.com/mahoshojoHCG/HITSC-Template/blob/master/README.zh_Hans.md)

## How to use it


``` shell
git clone https://github.com/mahoshojoHCG/HITSC-Template.git
git remote set-url origin $(YOUR_LAB_REPOSITORY_ADDRESS)
git remote -v
#verify if your remote has changed.
git push -u origin master
```

Everything will work automantic after you push.

**Don't forget to add source to `sourceSets` in `build.gradle` if you have more or less labs.**
