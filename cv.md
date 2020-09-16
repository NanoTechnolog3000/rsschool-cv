# Vitali Yaroshik

## Contact Info

* [Github](https://github.com/NanoTechnolog3000)
* [Gmail](yaroshik.vitali@gmail.com)
* [LinkedIn](https://www.linkedin.com/in/vitali-yaroshik-3ba7041b3/)


## Summary

QA Engineer with almost 3 years of practical experience in manual testing of mobile, web applications and hyperconverged infrastructure software. 

Well-organized and versatile team player. Key strengths include analytical and problem-solving skills, attention to details. Not afraid to take on new tasks and easily adapting to changing conditions of the project.
Familiar with the next programming languages: C#, Java, JavaScript.


## Skills

* **Platforms:** Microsoft Windows XP - 10, Linux (Ubuntu, CentOS), Android 2.x - 10.x, iOS 9.x - 13.x

* **Bug and Test Tracking Tools:** Atlassian Jira, TestRail

* **Databases:** MS SQL Server, MySQL Workbench, DataGrip

* **Programming Languages:** C#, Java, JavaScript

* **IDE:** Visual Studio, IntelliJ IDEA

* **Network Technologies:** TCP/IP, RDP, VPN, SSH, FTP

* **Other Technologies:** Virtualization, SOAP, REST, GraphQL, JSON, XML, SQL, etc.

* **Tools:** GIT, Postman, SoapUI, Fiddler, Charles, ADB, iTools, Unity, Oracle VM VirtualBox, Docker


## Code Example

```java
public class SearchLastFile {
    private static final SimpleDateFormat dateFormat = new SimpleDateFormat("yyyy-MM-dd hh:mm:ss");
    private static final int timeDifference = 10000;

    public static void printLastCreatedFiles(File[] files) {
        File lastFile = files[files.length - 1];

        System.out.printf("Список последних по дате создания файлов (+- %d секунд)%n", timeDifference / 1000);
        for (File file : files) {
            if (getFileCreationDate(lastFile) - getFileCreationDate(file) < timeDifference) {
                printFileInfo(file);
            }
        }
    }

    public static void sortByCreationDate(File[] files) {
        Arrays.sort(files, (f1, f2) -> {
            long l1 = getFileCreationDate(f1);
            long l2 = getFileCreationDate(f2);
            return Long.compare(l1, l2);
        });
    }

    private static long getFileCreationDate(File file) {
        try {
            BasicFileAttributes attr = Files.readAttributes(file.toPath(), BasicFileAttributes.class);
            return attr.creationTime().toInstant().toEpochMilli();
        } catch (IOException e) {
            throw new RuntimeException(file.getPath(), e);
        }
    }

    private static void printFileInfo(File file) {
        long fileCreationDate = getFileCreationDate(file);
        String formattedDate = dateFormat.format(new Date(fileCreationDate));
        System.out.printf("%s -> %s%n", file.getName(), formattedDate);
    }
}
```


## Experience

**Oct 2017 - Present**  
**Quality Assurance Engineer**  
*a1qa Software Testing Company, Minsk*  
Functional testing of different varieties of mobile, web applications, and hyperconverged infrastructure software. Running lectures and workshops - mentoring, providing feedback 


## Education

**2012 - 2017**  
**Bachelor of Engineering: Nanotechnologies and Nanomaterials in Electronics**  
*Belarusian State University of Informatics and Radioelectronics - Minsk*  
	

## Languages

* Belarussian
* Russian 
* English (B1 - Intermediate)
