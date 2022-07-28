# aaru

package Screenshot_demo_24_07;

import java.io.File;

import org.openqa.selenium.OutputType;
import org.openqa.selenium.TakesScreenshot;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.io.FileHandler;

public class Screenshot {

	public static void main(String[] args) throws Exception {
		// TODO Auto-generated method stub
		
		WebDriver driver;  
		
		System.setProperty("WebDriver.chrome,driver", "chromedriver.exe");
		driver = new ChromeDriver();
		driver.get("https://www.google.com/search?q=software+testing&rlz=1C1CHBF_enIN996IN996&oq=software+testing&aqs=chrome..69i57j0i512j0i433i512j0i433i457i512j0i402j0i512j0i433i512j0i512l3.10616j0j7&sourceid=chrome&ie=UTF-8");
		
		takeSnapShot (driver,"screenshotdemo(1)/sachin100.png");
		
		
		
		//= new ChromeDriver ();
		//driver.get("https://www.google.com/search?q=software+testing&rlz=1C1CHBF_enIN996IN996&oq=software+testing&aqs=chrome..69i57j0i512j0i433i512j0i433i457i512j0i402j0i512j0i433i512j0i512l3.10616j0j7&sourceid=chrome&ie=UTF-8");
       // driver.manage().window().maximize();
       // driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(100));
      
	}

	public static void takeSnapShot(WebDriver driver, String filewithpath) throws Exception {
		
		
		// TODO Auto-generated method stub
		
		TakesScreenshot scrShot = ((TakesScreenshot)driver);
		 File SrcFile = scrShot.getScreenshotAs(OutputType.FILE);
		
		File DestFile=new File(filewithpath);
		FileHandler.copy(SrcFile, DestFile);
		

	}

}
