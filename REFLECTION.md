# Reflection

_Task 4: The Reflection_

## 1. Describe the path an HTTP Request takes from a browser to your GitHub Pages site.

When someone types `https://batahualpa11.github.io` into a browser (or clicks a link to it),
the request goes through the following stages before the page appears on screen:

1. **URL parsing.** The browser parses the URL and determines the scheme (`https`), the
   host (`batahualpa11.github.io`), and the path (`/`).
2. **DNS resolution.** The browser needs an IP address for `batahualpa11.github.io`. It checks
   its local cache, then the OS resolver, then (if needed) queries a recursive DNS server, which
   walks the domain hierarchy (root → `.io` TLD → GitHub's authoritative name servers) until it
   resolves to the IP address(es) of GitHub Pages' hosting infrastructure.
3. **TCP connection.** The browser opens a TCP connection to that IP address on port 443,
   completing the three-way handshake (SYN → SYN-ACK → ACK).

