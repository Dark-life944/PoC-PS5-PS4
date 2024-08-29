# FilesystemEoPs

Exploit code for several techniques for taking advantage of filesystem-based exploit primitives.

* FolderOrFileDeleteToSystem: If you have an arbitrary folder or file delete as SYSTEM or admin, this exploit turns it into an EoP to SYSTEM.
  
  Credit: Abdelhamid Naceri (halov).
  
* FolderContentsDeleteToFolderDelete: If you have a delete of the contents of an arbitrary folder as SYSTEM/admin, or a recursive delete of a fixed but attacker-writable folder as SYSTEM/admin, this exploit turns it into an arbitrary folder delete as SYSTEM/admin. 
  
  Credit: Abdelhamid Naceri (halov).

These two can be chained together. Run FolderOrFileDeleteToSystem and wait to be prompted to trigger a folder delete. Then run FolderContentsDeleteToFolderDelete.

### Known Issues and Usage Notes

* FolderOrFileDeleteToSystem: Bitness must match the target system.

* You can use FolderOrFileDeleteToSystem even if your arbitrary file/folder delete vuln works asynchronously, for example, with a system restart. FolderOrFileDeleteToSystem operates in two stages. Stage 1 executes before you trigger the delete, and stage 2 executes after you trigger the delete. Use the `/stage1only` command-line flag to force FolderOrFileDeleteToSystem to exit after completing just stage 1; otherwise it will wait for you to trigger the delete (see console output for further instructions). If you stop after stage 1, then simply re-run FileOrFolderDeleteToSystem after you have triggered the delete. It will automatically detect this and skip immediately to stage 2.

* By contrast, FolderContentsDeleteToFolderDelete cannot work with an asynchronous delete vuln. The folder contents delete vuln must be triggered while FolderContentsDeleteToFolderDelete is running.



