#Overview

This Python project utilizes a producer-consumer model to fetch HTML content from a list of URLs and extract hyperlinks from them. 

#Features

Concurrent Execution: Both producer and consumer functions run in separate threads.
Queue-based Communication: A "None" marker is used for proper communication between threads.
Error Isolation: Exception handling ensures that one failed operation doesn't affect others.
Unit Testing: Includes unit tests for key functionalities.
Queue Size Management: The producer trims the oldest queue entries if the queue size balloons.

#Approach

Producer: Utilizes multiple threads to fetch HTML content from URLs and queue it.
Consumer: Reads the enqueued HTML content, parses it to extract hyperlinks, and stores them in an output dictionary.

#Assumptions

Libraries such as "requests" and "BeatifulSoup4" might not be present in all systems, provided a "pip install" at the beginning of the notebook if libraries are missing. The URLs provided are well-formed, with scraping TOS in mind.
Network latency and failures are possible, and the code is designed to handle such scenarios properly.

#Improvements

Rate Limiting: Introduce rate limiting to avoid overloading servers.
Logging: Add detailed logging for better debugging and monitoring.
