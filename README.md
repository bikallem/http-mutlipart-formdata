# http-mutlipart-formdata

A library which enables HTTP file uploads in ocaml web applications. HTTP file upload requests are generally encoded as `multipart/form-data` media content type. The library provides a simple api to parse and process such requests.

The parser implements HTTP `multipart/form-data` standard as defined in [RFC 7578](https://tools.ietf.org/html/rfc7578).

[API Documentation](https://lemaetech.co.uk/http-mutlipart-formdata/)

## Installation

```sh
$ opam install http-multipart-formdata
```

## Examples

```ocaml
open Http_multipart_formdata

let mp = Multipart.parse ~content_type_header ~body in
let file1_parts :  = Multipart.Map.find "file1" mp
```

[Full API Usage](https://github.com/lemaetech/http-mutlipart-formdata/blob/master/test/test.ml)
