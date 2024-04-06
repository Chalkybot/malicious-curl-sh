# This is a simple demonstration of how utilizing cat and curl can leave you vulnerable
As cat and curl both render escape characters accurately without special flags, these can be used to maliciously hide code in shellscripts.
The evil_script.sh file demonstrates this by hiding code using escape characters. If you wish to use cat to display the file, you may use ``cat -vet`` to not render the escape characters.
