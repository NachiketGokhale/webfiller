import datetime
import time
from selenium import webdriver

# Set the desired date and time for filling out the form
desired_date = datetime.datetime(2023, 3, 27, 0, 45, 0) # format: year, month, day, hour, minute, second

# Loop until the current date and time match the desired date and time
while datetime.datetime.now() < desired_date:
    time.sleep(1)

# Once the desired time is reached, use Selenium to navigate to the website and fill out the form
driver = webdriver.Chrome()
driver.get('https://www.iitk.ac.in/mse/sem/slot_book11.html')
driver.find_element_by_name('name').send_keys('Nachiket Gokhale')

dropdown = Select(driver.find_element_by_name('I am from:'))
dropdown.select_by_value('Chemical Engineering')

driver.find_element_by_name('rollorPF').send_keys('18102278')

driver.find_element_by_name('email').send_keys('ngokhale@iitk.ac.in')
driver.find_element_by_name('mobile').send_keys('7588401580')
dropdown = Select(driver.find_element_by_name('month'))
dropdown.select_by_value('April')       #Add the month
dropdown = Select(driver.find_element_by_name('date'))
dropdown.select_by_value('06')    #Add the date
dropdown = Select(driver.find_element_by_name('year'))
dropdown.select_by_value('2023')     #Add the year

driver.find_element_by_name('submit').click()
driver.quit()
