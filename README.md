# multiReleaseJars
gilde meeting

Links met info:
https://blog.jetbrains.com/idea/2017/10/creating-multi-release-jar-files-in-intellij-idea/
https://www.javaworld.com/article/3184029/java-language/java-9s-other-new-enhancements-part-4-multi-release-jar-files.html?page=2

## How?
Manifest.mf: Multi-Release: true 

```
JAR content root
    A.class
    B.class
    C.class
    D.class
    META-INF
        MANIFEST.mf
        versions
            9
                A.class
                B.class
            10
                A.class
```

## Pro's
* New features can be used while remaining compatible with old versions
* One jar for different versions of java
* Users of the libraries are not forced to stick to a specific version of the library if they cannot upgrade java

## Con's
* Different versions have to be maintained
* Compilation with different target-versions

## When to use
* Library development
* Migration to new version of Java
