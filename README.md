# Bookmark Server
A bookmark server or URI shortener maintains a mapping (dictionary) between short names and long URIs, checking that each new URI added to the
mapping actually works (i.e. returns a 200 OK).
# Features

This server is intended to serve three kinds of requests:
1. A GET request to the / (root) path.  The server returns a form allowing the user to submit a new name/URI pairing.  The form also includes a listing of all the known pairings.
2. A POST request containing "longuri" and "shortname" fields.  The server checks that the URI is valid (by requesting it), and if so, stores the mapping from shortname to longuri in its dictionary.  The server then redirects back to the root path.
3. A GET request whose path contains a short name.  The server looks up that short name in its dictionary and redirects to the corresponding long URI.
# Installation

1. Download the files.
2. Run BookmarkServer.py

