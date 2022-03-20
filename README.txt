This is a backport of some important additions to ioquake3 to Tremulous 1.1.0.

A backport is required because the current Tremulous client built from SVN
is no longer compatible with the 1.1.0 data files and vms.

This is based on the Tremulous SVN version 755 with the following additions:

* cl_guid (because I'm a shameless self promoter)
* May 8, 2006 security fix for COM_StripExtension()
  http://lists.grok.org.uk/pipermail/full-disclosure/2006-May/045906.html
* WinXP SP2 NX-extension fix
* June 2, 2006 security fix
  http://www.derkeiler.com/Mailing-Lists/Full-Disclosure/2006-06/msg00112.html
* R1CH's Alt-Tab fix (you need to set win_allowAltTab 1 for this to work)
* win32 builds add a "home path" in /Documents and Settings
* cURL support for HTTP/FTP downloads.  cl_allowDownload and cl_wwwDownload
  both need to be set to 1 (the server also needs to be patched and configured
  for this to work).
* OpenAL sound tracking fix (bug 2893)
* added cl_guidServerUniq.  When set to non-zero a different cl_guid is sent
  to each server you connect to to prevent guid theft by malicious server
  admins.

I strongly recommend backing up your existing binaries in case these 
don't work out.

