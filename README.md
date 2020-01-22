# My-selenium
Edit Box
package editbox;

import org.openqa.selenium.Alert;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.remote.server.handler.FindElement;

public class Edit_Box_one {

	public static void main(String[] args) throws InterruptedException {
		System.setProperty("webdriver.chrome.driver", "F:\\selinum floder\\chromedriver.exe");
		WebDriver driver=new ChromeDriver();

		driver.get("http://www.leafground.com/pages/Edit.html");
		WebElement emailbox=driver.findElement(By.id("email"));
		emailbox.click();
		emailbox.sendKeys("karthikeyan");
		WebElement append=driver.findElement(By .xpath("//*[@id=\'contentblock\']/section/div[2]/div/div/input"));
		append.click();
		append.sendKeys("karthikeyan");
		Thread.sleep(5000);
		WebElement getText=driver.findElement(By.xpath("//*[@id=\"contentblock\"]/section/div[3]/div/div/input"));
		String thetextis1=getText.getAttribute("value");
		System.out.println(thetextis1);

		WebElement clear1=driver.findElement(By.xpath("//*[@id=\"contentblock\"]/section/div[4]/div/div/input"));
		clear1.clear();

		WebElement enableornot=driver.findElement(By.xpath("//*[@id=\"contentblock\"]/section/div[5]/div/div/input"));
		boolean status =enableornot.isEnabled();
		System.out.println(status);

		emailbox.click();
		Thread.sleep(5000);
		emailbox.sendKeys(" 2  Time Feeding Email Id");
		driver.get("http://www.leafground.com/home.html");
		driver.findElement(By.xpath("//*[@id=\"post-153\"]/div[2]/div/ul/li[9]/a")).click();
		driver.findElement(By.xpath("//*[@id=\"contentblock\"]/section/div[1]/div/div/button")).click();
		WebElement no1=driver.findElement(By.xpath("http://www.leafground.com/home.html"));
		no1.click();
		WebElement no2=driver.findElement(By.xpath("//*[@id=\"post-153\"]/div[2]/div/ul/li[16]/a/img"));
		no2.click();
		driver.navigate().to("http://www.leafground.com/home.html");
		WebElement alert1=driver.findElement(By.xpath("//*[@id=\"post-153\"]/div[2]/div/ul/li[9]/a"));
		alert1.click();
		WebElement alertbox1=driver.findElement(By.xpath("//*[@id=\"contentblock\"]/section/div[1]/div/div/button"));
		alertbox1.click();
		Alert alert=driver.switchTo().alert();
		Thread.sleep(2000);
		alert.accept();
		WebElement alertbox2=driver.findElement(By.xpath("//*[@id=\"contentblock\"]/section/div[2]/div/div/button"));
		alertbox2.click();
		Alert alert2=driver.switchTo().alert();
		alert2.accept();
		Thread.sleep(5000);
		WebElement alertbox4=driver.findElement(By.xpath("//*[@id=\"contentblock\"]/section/div[3]/div/div/button"));
driver.manage().window().maximize();
driver.manage().window().fullscreen();
		driver.navigate().to("https://accounts.google.com/signup/v2/webcreateaccount?service=mail&continue=https%3A%2F%2Fmail.google.com%2Fmail%2F&flowName=GlifWebSignIn&flowEntry=SignUp");
		WebElement no9=driver.findElement(By.xpath("//*[@id=\"firstName\"]"))	;
		no9.click();
		no9.sendKeys("KARTHIKEYAN");
		WebElement no6=driver.findElement(By.xpath("//*[@id=\"lastName\"]"));
		no6.click();
		no6.sendKeys("k");
		WebElement no3=driver.findElement(By.xpath("//*[@id=\"username\"]"));
		no3.click();
		no3.clear();
		no3.sendKeys("karthikeyangptmech1998");
		WebElement no4=driver.findElement(By.xpath("//*[@id=\"passwd\"]/div[1]/div/div[1]/input"));
		no4.click();
		no4.sendKeys("12345678");
		WebElement no5=driver.findElement(By.xpath("//*[@id=\"confirm-passwd\"]/div[1]/div/div[1]/input"));
		no5.click();
		no5.sendKeys("12345678");
		WebElement no8=driver.findElement(By.xpath("//*[@id=\"accountDetailsNext\"]/span/span"));
		no8.click();


driver.quit();
	}

}
