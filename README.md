This is a microservice for scraping logos and images off of Wikipedia.

It communicates with other programs through the 'signal.txt' file that is located in this directory.

If you wish to make a request, write the following to the 'signal.txt' file:
the word "image" or "logo", then the URL of the Wikipedia page that this image or logo is featured on.

EXAMPLE REQUESTS:

    image https://en.wikipedia.org/wiki/Oregon_State_University
    
    logo https://en.wikipedia.org/wiki/Apple_Inc.

Requests will generate an 'output.png' file with the scraped image or logo. This 'output.png' file will be erased upon the next request, 
so be sure to save it if you wish to use it for long-term purposes.

The request made in the 'signal.txt' file will also be erased after it has been read by the 'wiki_scraper.py' file, so your program
only needs to write to 'signal.txt'; it does not have to erase past requests before writing new ones.

If no image is found on the given Wikipedia page, the 'wiki_scraper.py' file will print out "Image not found." It is still able to
take new requests after this occurs.

NOTES:

A request for an image is less specific than a request for a logo, so sometimes scraped images are also logos.

If you encounter an error that says "certificate verify failed: unable to get local issuer certificate", you likely need to install the "Install Certificates.command" file located in your Python download directory for this microservice to operate correctly. This is done by simply double clicking the "Install Certificates.command" file. More information on this can be found here: https://stackoverflow.com/questions/52805115/certificate-verify-failed-unable-to-get-local-issuer-certificate.
