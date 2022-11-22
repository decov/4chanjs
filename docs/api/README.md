# 4chan api / docs #
#### welcome to the documentation for 4chan's read-only json api, originally launched in september of 2012.
----
## getting started
data from the 4chan api is exclusively accessible from `a.4cdn.org`, via either `http://` or `https://` protocols. `a.4cdn.org` serves json representations of posts made at [`4chan.org`](https://4chan.org/) and [`4channel.org`](https://4channel.org/) boards. all examples in the documentation for the 4chan api use `https://`.

[CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) is supported from origins `boards.4chan.org` or `boards.4channel.org`, via `http://` or `https://`. requests are accepted when using the following http request types:
  - [`GET`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/GET)
  - [`OPTIONS`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/OPTIONS)
  - [`HEAD`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/HEAD)

### table of contents ###

| **documentation page**   | **description**      |
|:-------------------------|:---------------------|
| [endpoints and site domains](pages/Endpoints_and_domains.md) | A quick rundown of all 4chan API endpoints and site domains.|
| [media and static content](pages/User_images_and_static_content.md) | Paths and locations for static site content including custom spoiler images, country flags, capcodes and user submitted media |
| [archive.json](pages/Archive.md) | documentation for the 4chan native archive and its json |
| [boards.json](pages/Boards.md) | documentation for the 4chan board list and its attributes |
| [catalog.json](pages/Catalog.md) | documentation for the json representation of the 4chan native catalog |
| [index endpoint](pages/Indexes.md) | documentation for the json representaion of board index (main) pages |
| [thread endpoint](pages/Threads.md) | documentation for the json representation of specific 4chan threads |
| [thread list](pages/Threadlist.md) | documentation for the board threadlist and its brief stats |

### api / rules ###

1. do not make more than one request per second. 
2. thread updating should be set to a minimum of 10 seconds, preferably higher.
3. use [if-modified-since](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/If-Modified-Since) when doing your requests.
4. make api requests using the same protocol as the app. only use ssl when a user is accessing your app over https.

### api / terms of service ###

1. you may not use "4chan" in the title of your application, product, or service.
2. you may not use the 4chan name, logo, or brand to promote your application, product, or service.
3. you must disclose the source of the information shown by your application, product, or service as 4chan, and provide a link.
4. you may not market your application, product, or service as being "official" in any way.
5. you may not clone 4chan or its existing features/functionality. example: don't suck down our json, host it elsewhere, and throw ads around it.
6. these terms are subject to change without notice.

-------

to view a pretty-printed version of our thread, index, and catalog json, use [jsonlint](http://jsonlint.com).

still have questions or concerns? open an issue or email [api@4chan.org](mailto:api@4chan.org)
