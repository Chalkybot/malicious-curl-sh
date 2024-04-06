# This is a simple demonstration of how code can be hidden using escape characters.
As cat and curl both render escape characters accurately without special flags, these can be used to maliciously hide code in shellscripts.

The evil_script.sh file demonstrates this by hiding code using escape characters. If you wish to use cat to display the file, you may use ``cat -vet`` to not render the escape characters.

As curl does the same, if a user first curls the script to check the contents, then pipes the output straight to sh with``curl example.org/script.sh | sh``, this would lead to unintended code being executed on the system.

The sites-available folder contains an example nginx configuration to serve a different site to curl and other user-agents, this could potentially further hide the malicious code as it'd only be served to the clients using the curl user-agent.
