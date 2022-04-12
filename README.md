<h1 align="center">
  <br>
  <a href="https://github.com/scaninfoga/CSRF-Scanner"><img src="http://scaninfoga.in/wp-content/uploads/2022/01/cropped-cropped-scaninfoga.png" alt="CSRF-Scanner"></a>
  <br>
  CSRF-Scanner
  <br>
</h1>

<h4 align="center">A dumb CSRF scanner</h4>

<p align="center">
  <a href="https://github.com/scaninfoga">
    <img src="http://scaninfoga.in/wp-content/uploads/2022/01/globe-free-img.png">
  </a>
  <a href="https://www.instagram.com/rohan_nahak.h.r/">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Instagram_icon.png/2048px-Instagram_icon.png">
  </a>
</p>

![demo](http://scaninfoga.in/wp-content/uploads/2022/04/scaninfoga-123.png)

### Important
CSRF-Scanner is in beta phase of development which means there can be bugs. Any production use of this tool discouraged.
Pull requests and issues are welcome. I also suggest you to put this repo on watch if you are interested in it.

### Workflow

#### Crawling
CSRF-Scanner crawls the target website to the specified depth and stores all the HTML forms found in a database for further processing.

#### Evaluating
In this phase, CSRF-Scanner finds out the tokens which aren't strong enough and the forms which aren't protected.

##### Observing
In this phase, 100 simultaneous requests are made to a single webpage to see if same tokens are generated for the requests.

##### Testing
This phase is dedicated to active testing of the CSRF protection mechanism. It includes but not limited to checking if protection exsists for moblie browsers, submitting requests with self-generated token and testing if token is being checked to a certain length.

##### Analysing
Various statistical checks are performed in this phase to see if the token is really random.
Following tests are performed during this phase
- Monobit frequency test
- Block frequency test
- Runs test
- Spectral test
- Non-overlapping template matching test
- Overlapping template matching test
- Serial test
- Cumultative sums test
- Aproximate entropy test
- Random excursions variant test
- Linear complexity test
- Longest runs test
- Maurers universal statistic test
- Random excursions test

### Usage

Scanning a website for using CSRF-Scanner is as easy as doing
```
python3 bolt.py -u https://facbook.com -l 2
```
Where `-u` is used to supply the URL and `-l` is used to specify the depth of crawling.

Other options and switches:

- `-t` number of threads
- `--delay` delay between requests
- `--timeout` http request timeout
- `--headers` supply http headers


