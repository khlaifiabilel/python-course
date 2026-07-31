# Introduction to Python Course

A static, browser-based collection of eight introductory Python slide decks
with a legacy Dialogflow/API.AI chatbot shell on the landing page.

**Published site:** <https://khlaifiabilel.github.io/python-course/>

**Status:** Historical course material. The slide exports and legacy chatbot
shell are retained as a reference, not maintained as a current Python
curriculum or chatbot integration.

## Course material

The exported HTML decks cover a progression from programming and Python basics
through practical language topics. Open `index.html` to reach classes 1 through
8, or open any `Python courseNN.html` file directly.

This repository contains presentation material, not an installable Python
package. `requirements.txt` is empty, and no Python interpreter or package
installation is needed to view the lessons.

## Run locally

Some pages load fonts, images, jQuery, or other assets from external hosts, so
serve the directory over HTTP and remain online for the complete presentation:

```bash
git clone https://github.com/khlaifiabilel/python-course.git
cd python-course
python3 -m http.server 8000
```

Open <http://127.0.0.1:8000/>. The course pages are static; the `python3` command
is only being used as a convenient local web server.

## Chatbot status

The landing page includes a `<mybot>` widget implemented by
`assets/js/script.js` and historical branding for API.AI, the predecessor of
Dialogflow. There is no current Dialogflow agent configuration or secret in the
repository. Treat the chatbot as legacy presentation code; it may not function
against current services.

## Pages and repository identity

GitHub Pages is built from the root of `master` at the published URL above. The
older repository metadata and in-page ribbon still refer to the previous
`KalifiaBillal/Introduction-to-Python-Programming-language` identity; the
canonical repository is now `khlaifiabilel/python-course`. No Pages or
repository rename is required to use the current URL.

The committed Jekyll workflow also builds on pushes and pull requests to
`master`, but it uses `actions/checkout@v2` and a floating
`jekyll/builder:latest` container. That historical workflow should not be
treated as a reproducible modern toolchain.

## Verification

There is no automated course-content test suite. Appropriate checks are:

- open the landing page and each of the eight course links;
- confirm local CSS, JavaScript, image, and font paths resolve;
- navigate slides with keyboard controls and test at desktop/mobile widths;
- review browser developer tools for failed third-party resources.

No student code is executed, graded, or submitted by this site.

## Provenance

The repository history begins with an import by `kalifiabillal` on 2020-06-02,
and the slide exports identify Kalifia Billal as author. The exported decks
embed Reveal.js and other browser libraries with their retained copyright and
license comments. External images and fonts remain hosted by their respective
providers and are not original repository assets merely because they are
referenced by a slide.

## Known limitations

- Examples reflect the Python 3.8-era course and should be checked against a
  currently supported Python release.
- The chatbot integration is obsolete and unconfigured.
- Many large slide dependencies are embedded in generated HTML, making the
  source difficult to maintain by hand.
- Availability and licensing of externally hosted media can change.

## License

The root [`LICENSE`](LICENSE) applies the MIT License to repository material
copyright Bilel Khlaifia. Embedded Reveal.js and other third-party components
retain their own copyright and license notices; the repository-level license
does not replace those terms.
