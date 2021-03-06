# Bundle: Cascade Delete

The cascade delete bundle allows a specified set of documents and attachments to be deleted when the document that owns it is deleted. Typical usage scenarios include deleting an attachment that is referenced by a document or removing a set of child documents referenced by a parent document.

## Installation

Simply place the Raven.Bundles.CascadeDelete.dll (included in RavenDB distribution package) in the `Plugins` directory.

## Usage

You can specify the documents and attachments to be cascade deleted using the following code:

{CODE cascadedelete1@Server\Extending\Bundles\CascadeDelete.cs /}

When the "parent" document is deleted, the documents with IDs "childId1" and "childId2" and the attachments with IDs "attachmentId1" and "attachmentId2" will be deleted as well.

**Notes:**

1. The "Raven-Cascade-Delete-Documents" and "Raven-Cascade-Delete-Attachments" collections are independent of each other; a document can specify from zero to any number of either documents or attachments to be cascade deleted.
2. Cascade Delete works only within a single node. If you have a sharded data set, cascading will not delete documents / attachments that are located on other nodes.
