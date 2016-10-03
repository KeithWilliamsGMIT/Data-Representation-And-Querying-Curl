# Answers for curl problem sheet
## Problem 2
After downloading http://www.jmarshall.com/easy/http/ I used a file redirect (>) to save it to http-easy.html. I noticed the image in the top left wasn't displayed because it had a relative src.

## Problem 3
I used the -L (--location) flag because the requested page had been moved to a different location. The -L flag will make curl redo the request on the new place.

Using the -v (--verbose) flag, as required in the question, curl returned the http headers and the body. I also experimented with the -I (--head) flag which only returned the http headers.

The -s (--silent) flag didn't return any progress bars.

I also had to add 2>&1 to the end of the command to combine stderr and stdout so I could output the results to a file.

## Problem 4
Similar to the previous problems but the URL had to be wrapped in quotes due to the ampersand in the parameter list.

## Problem 5
I had to wrap the URL in quotes because of the ampersand in the parameter list like in problem 4.

I piped the result to the python json.tool module to format it before outputting to the file gmit.json.

## Problem 6
I started the python SimpleHTTPServer without specifying a port number which defaults to 8000. I then used curl to access the page at http://localhost:8000/index.html.

I downloaded the files from the CDN, similar to the previous problems.
