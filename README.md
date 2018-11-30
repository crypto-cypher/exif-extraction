# exif-extraction
Techniques for extracting metadata from files &amp; sorting it into a spreadsheet using exiftool.

**PDF:**
$ exiftool -csv -title -author -creator -creatortool -pagecount -pdfversion -createdate -modifydate -r -ext pdf . > exif-pdf.csv

**DOCX:**
$ exiftool -csv -title -creator -lastmodifiedby -company -application -template -words -appversion -docsecurity -createdate -modifydate -r -ext docx . > exif-docx.csv

**PPT:**
$ exiftool -csv -title -titleofparts -currentuser -author -lastmodifiedby -company -software -codepage -words -notes -appversion -createdate -modifydate -r -ext ppt . > exif-ppt.csv

**XLS:**
$ exiftool -csv -title -Tag_AuthorEmailDisplayName -Tag_AuthorEmail -Tag_EmailSubject -lastmodifiedby -codepage -appversion -security -createdate -modifydate -r -ext xls . > exif-xls.csv

**XLSX:**
$ exiftool -csv -TitlesOfParts -HeadingPairs -Creator -LastModifiedBy -Application -DocSecurity -AppVersion -CreateDate -ModifyDate -r -ext .xlsx . > exif-xlsx.csv

**View a file's metadata:**
$ exiftool -a -u -g2 -s <file.type>

The -s comand will tell you the raw metadata tag title to reference when calling field elements.
