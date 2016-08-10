# MoveIt! Documentation

This is the source for MoveIt! Motion Planning framework documentation which is hosted at http://moveit.ros.org/

Building New Releases
---------------------

Install prerequisites:

```
sudo pip install sphinx
```

Build new release from master, store into gh-pages branch:

```
git checkout master
make html
make latexpdf
git checkout gh-pages
cp -r build/html/* .
cp build/latex/MoveIt.pdf .
rm -rf build
git commit -a "new build"
git push origin gh-pages
```

Troubleshooting:

If you get complaints about .sty files install the following

```
sudo apt-get install texlive-full
```
