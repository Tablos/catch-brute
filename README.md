# Catch
Catch is a brute force tool that is used to brute force most websites

# Update! recoded by Tablos
You can run Catch with python3 now.
The main purpose of this fork is to improve the number of passwords tested by second.
The original code call a two-second sleep between each try, I replace this by the 'wait until presence of element located'

time.sleep(2) -> wait.until(EC.presence_of_element_located((By.CSS_SELECTOR, login_btn_selector)))

The process is two times faster with this modification.

# Update! v.1.3
added arg support **yay**
<br>
  -h, --help            show this help message and exit<br>
  -u USERNAME, --username=USERNAME Choose the username<br>
  --usernamesel=USERNAMESEL Choose the username selector<br>
  --passsel=PASSSEL     Choose the password selector<br>
  --loginsel=LOGINSEL   Choose the login button selector<br>
  --passlist=PASSLIST   Enter the password list directory<br>
  --website=WEBSITE     choose a website<br>
dont worry if you load up the tool without any args youll go to the default wizard!
Also i removed the apt xvfb and pip2 pyvirtualdisplay
## Installation Instructions

first:

download the browser

https://chromium.cypress.io/linux/stable/93.0.4577.63

second

download the chromedriver 

https://www.googleapis.com/download/storage/v1/b/chromium-browser-snapshots/o/Linux_x64%2F902218%2Fchromedriver_linux64.zip?generation=1626393410465443&alt=media

unzip Linux_x64_902218_chromedriver_linux64.zip

cd chromedriver_linux64/ && chmod 777 chromedriver && mv * /bin

##

Now for install the tool type

```
git clone https://github.com/Tablos/catch-brute

chmod 777 install.sh

sudo ./install.sh

sudo catch
```
chrome driver and chrome are also required!
link to chrome driver: http://chromedriver.chromium.org/downloads
copy it to bin!
<br>
## How to use (text)
1). Find a website with a login page<br>
2). Inspect element to find the Selector of the username form<br>
3). Do the same for the password field<br>
4). The the login form <br>
5). When Asked put in the username to brute force<br>
6). Watch it go!
