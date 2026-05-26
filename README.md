# 🖥️ Sprint 8 — Web Test Automation with Selenium (Urban Routes)

## 🤖 Project Overview

This sprint focuses on implementing end-to-end test automation for the Urban Routes web application using Selenium WebDriver and the Page Object Model (POM) design pattern. The goal is to automate the complete taxi request flow from start to finish, simulating a real user journey.

## 🎯 Sprint Objectives

- Add setup and teardown methods in main.py  
- Implement Page Object Model structure in pages.py  
- Define locators and Selenium actions  
- Complete automated test cases in main.py  
- Execute tests using Pytest framework  

## 🧪 Test Structure (main.py)

class TestUrbanRoutes:

    @classmethod
    def setup_class(cls):
        if helpers.is_url_reachable(data.URBAN_ROUTES_URL):
            print("Connected to Urban Routes server")
        else:
            print("Unable to connect to Urban Routes. Please check the server.")

    @classmethod
    def teardown_class(cls):
        print("Finishing Urban Routes test execution")

    def test_set_route(self): ...
    def test_select_plan(self): ...
    def test_fill_phone_number(self): ...
    def test_fill_card(self): ...
    def test_comment_for_driver(self): ...
    def test_order_blanket_and_handkerchiefs(self): ...
    def test_order_2_ice_creams(self): ...
    def test_car_search_model_appears(self): ...

## 🧱 Page Object Model (pages.py)

from selenium.webdriver.common.by import By

class UrbanRoutesPage:

    ADDRESS_FROM = (By.ID, "address_from")  
    ADDRESS_TO = (By.ID, "address_to")  
    PHONE_NUMBER = (By.ID, "phone")  
    CARD_NUMBER = (By.ID, "card")  
    CARD_CODE = (By.ID, "code")  
    MESSAGE_FOR_DRIVER = (By.ID, "comment")  
    ICE_CREAM_BUTTON = (By.CLASS_NAME, "ice-cream")  
    BLANKET_BUTTON = (By.CLASS_NAME, "blanket")  
    COMFORT_PLAN = (By.ID, "comfort_plan")  
    CAR_SEARCH_MODAL = (By.ID, "car_search")  

    def set_route(self, driver, from_addr, to_addr): ...  
    def select_plan(self, driver): ...  
    def fill_phone(self, driver, phone): ...  
    def fill_card(self, driver, card, code): ...  
    def comment_for_driver(self, driver, message): ...  
    def order_ice_cream(self, driver, times=2): ...  
    def order_blanket(self, driver): ...  
    def verify_car_modal(self, driver): ...  

## 🧠 Key Concepts Used

- Selenium WebDriver  
- Page Object Model (POM)  
- Test Automation Structure  
- Pytest Framework  
- End-to-End UI Testing  

## 🚀 Outcome

This project demonstrates the ability to design and implement automated UI tests for a real-world web application, covering the full user journey of requesting a taxi. It establishes a strong foundation for scalable test automation using Selenium.

## ⭐ Author

Fernanda Carneiro Alves — Junior QA Engineer
