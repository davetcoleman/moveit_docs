# MoveIt! Documentation

This is the source for MoveIt! Motion Planning framework documentation. For now it is hosted within this repo:

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
