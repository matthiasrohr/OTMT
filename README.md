# Open Threat Modeling Templates

The aim of this site is to provide guidance around <a href="http://aka.ms/tmt2016">Microsofts Threat Modeling Tool</a> and to share templates and models. Threat Modeling Tool is a free windows based tool that can be used within a threat modeling activity. As of version 2016, is offers strong customization capability allowing to map your own threat logic and stencils to it.

This site was created as part of an talk of Matthias Rohr at OWASP AppSec EU 2016.

<b>Useful URLs:</b>
- Download: http://aka.ms/tmt2016
- CommunityUrl: http://social.msdn.microsoft.com/Forums/en-US/sdlprocess/threads
- SdlUrl: http://www.microsoft.com/security/sdl
- TwCBlog: http://blogs.technet.com/b/trustworthycomputing
- MsdnForums: http://social.msdn.microsoft.com/Forums/en-US/home?forum=sdlprocess

<b>Assingning a new Templates to a Model:</b>

Each threat model has its own template (.tm7 file) assigned to it via a unique id. Unfortunately this ID cannot be changed from within the tool itself. To adapt a new template to an existing model you therefore need to change the template ID manually by opening the file within a text editor. Luckily, both template and model are XML based.

In the model, search for the manifest tag and change ID and Name to match the values as in the template file. Furthermore, change the Version to a value lower than the one in the template file.
For example, if the current version in the template file [secodis web plain.tb7](https://github.com/matthiasrohr/OTMT/blob/master/secodis%20web%20plain.tb7) is 1.0.0.228, set the following values in the model:
```xml
<a:Manifest>
   <a:Author>...</a:Author>
   <a:Id>aef9fb95-2bd6-4f3b-8325-62e83d6ccaa2</a:Id>
   <a:Name>Secodis Web Plain</a:Name>
   <a:Version>1.0.0.227</a:Version>
</a:Manifest>
```

Finally, open the model in the Microsoft Threat Modeling tool.
The tool may now detect that a new version of the template is available and directly ask you to update to the new version. If this is not the case, apply the model manually via "File -> Apply Template".
