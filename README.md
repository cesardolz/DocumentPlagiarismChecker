# Document Plagiarism Checker
This project contains a really simple way to compare a set of documents between each other in order to check if some of them are copies and it has been developed for academic purposes only.
## WARNING: still in an early development stage.
### How to use it:
#### As an stand-alone app:
Clone the repository to your local working directory, restore the dependencies with `dotnet restore` and build it with `dotnet build`. Finally run the project with `dotnet run %files_path %files_extension` where *%files_path* is the folder that contains all the documents to compare and *%files_extension* is the files's extension to check (files with other extensions will be ignored).
#### As a library:
Do the same as with the stand-alone app but import the compiled **DocumentPlagiarismChecker.dll** file to your project. Then invoke the **CompareFiles** method inside the **API** object to get the results. You can also send them to an output with the **WriteOutput** method inside the same **API** object.
### How to add new comparator:
New comparators will be added as long as the tool became improved with new capabilities but, if anyone wants to contribute or just code their own comparator, feel free to enjoy following those steps:
 1. Copy the **_tamplate** folder with all its content inside the **Comparators** folder.
 2. Rename the new folder with the name of your comparator.
 2. Correct the namespace of the copied folders and replace **_template** with the name of your comparator (must match the name of the folder).
 3. Code both files following the indications, but you can use the current comparators as a guide.
 ### List of comparators (marked ones are avaliables, the other ones are under development):
- [x] Document Word count: compares two PDF files and check how many words and how many times appears within each document, useful for checking if two documents are almost equals.
- [ ] Paragraph Word count: compares two PDF files and check how many words and how many times appears within each paragraph, useful for checking which parts of two documents are almost equals.
 ### Roadmap:
- [ ] Configuration file: some settings will be able to be established inside this file (comparators to use or ignore, folders, extensions, outputs, etc.).
- [ ] Sample file: the ability to set a sample file that will be used to ignore some comparisons, useful to exclude some homework statement from the plagiarism matching result.
### Changelog:
- v0.1.0.0 - 02/12/2018: Initial release.
