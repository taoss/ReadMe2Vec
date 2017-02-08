# ReadMe2Vec
ReadMe2Vec is a word embedding representation extracted from READMEs of Github projects.

Requirements:
 - OS: Linux 64-Bit

Dependencies:
 - Python 3 (64-Bit)
 https://www.python.org/downloads/source/
 - Numpy 1.11.2 (64-Bit)
 http://scipy.org/install.html#install-systemwide-via-a-linux-package-manager
 - Gensim 0.13.3 (64-Bit)
 http://radimrehurek.com/gensim/install.html

Installation:
First of all, you need to install Python 3 then install Numpy for Scientific and numerical computations. 
Finally,  you will install Gensim library. 

Note: ReadMe2Vec is tested on Ubuntu 64-Bit OS.

Example:
Before loading the ReadMe2Vec model, unrar "readme2vec.rar" file to a directory. The extension of extracted file is 'bin' 

```python
from gensim.models import word2vec
readme2vec = word2vec.Word2Vec.load_word2vec_format('readme2vec.bin', binary=True)
print(readme2vec.most_similar(positive=['junit', 'python'], negative=['java']))
```
output:
[('unittest', 0.5596792697906494),
 ('pytest', 0.539635181427002),
 ('nose', 0.533279538154602),
 ('setuptools', 0.5255333185195923),
 ('setup.py', 0.5000009536743164),
 ('test.py', 0.49264946579933167),
 ('run_tests.py', 0.48780664801597595),
 ('bootstrap.py', 0.4832579493522644),
 ('nosetests', 0.47157174348831177),
 ('python3', 0.4556870460510254)]
