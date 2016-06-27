# otmt
Open Threat Modeling Template

The aim of this site is to provide guidance around Microsofts Threat Modeling Tool and to share templates and models. Threat Modeling Tool is a free windows based tool that can be used within a threat modeling activity. As of version 2016, is offers strong customization capability allowing to map your own threat logic and stencils to it.

Useful URLs:
- Download: http://aka.ms/tmt2016
- CommunityUrl: http://social.msdn.microsoft.com/Forums/en-US/sdlprocess/threads
- SdlUrl: http://www.microsoft.com/security/sdl
- TwCBlog: http://blogs.technet.com/b/trustworthycomputing
- MsdnForums: http://social.msdn.microsoft.com/Forums/en-US/home?forum=sdlprocess


Assingning a new Templates to a Model:

Each threat model has its own template (.tm7 file) assigned to it via a unique id. Unfortunately this ID cannot be changed from within the tool itself. To adapt a new template to an existing model you therefore need to change the template ID manually by opening the file within a text editor. Lukily, both template and model are XML based.

Here, search for the manifest tag and change ID and name from the template file to it, e.g.:&lt;br/&gt;
&lt;a:Manifest&gt;&nbsp;&lt;a:Author&gt;MROHR-PC\mrohr&lt;/a:Author&gt;&lt;br/&gt;&nbsp; &lt;a:Id&gt;aef9fb95-2bd6-4f3b-8325-62e83d6ccaa2&lt;/a:Id&gt;&lt;br/&gt;&nbsp;&lt;a:Name&gt;Secodis Web Plain&lt;/a:Name&gt; &nbsp;&lt;a:Version&gt;1.0.0.227&lt;/a:Version&gt;&lt;br/&gt;&nbsp;&lt;/a:Manifest&gt;

Finally, open the template in the tool and apply the model manually via "File -> Apply Template"
