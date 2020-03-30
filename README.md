This jupyter notebook downloads all of the available [MFADT Thesis documents](https://digitalarchives.library.newschool.edu/index.php/Search/objects/search/PC020402) on The New School's library archive.

I used [pyenv](https://github.com/pyenv/pyenv) with anaconda3-2019.10 set as my version of python.

The final PDF directory is 8.3 GB so it was not checked into version control. Before uploading to google drive I compressed using gs.

```shell
# inside of the PDF directory
for i in $(ls); do gs -sDEVICE=pdfwrite -dPDFSETTINGS=/ebook -q -o ../compressed/$i $i; done
```