# ExtentManager Java Code

Link:http://extentreports.relevantcodes.com/java/#parallel-classes
Complete Java Code below:
import com.relevantcodes.extentreports.ExtentReports;

public class ExtentManager {
    static ExtentReports extent;
    final static String filePath = "Extent.html";
    
    public synchronized static ExtentReports getReporter() {
        if (extent == null) {
            extent = new ExtentReports(filePath, true);
        }
        
        return extent;
    }
}
