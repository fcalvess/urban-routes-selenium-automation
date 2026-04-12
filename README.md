Sprint 8 — Automação de Testes de Aplicativos Web 🖥️🤖

📝 Descrição do Sprint
Finalização do script de teste automatizado do Urban Routes usando Selenium e POM (Page Object Model). O objetivo é executar todo o fluxo de solicitação de um táxi de ponta a ponta.

🎯 Objetivos do Sprint

Adicionar setup e teardown no main.py

Criar classe de página (pages.py) usando POM

Implementar localizadores e métodos Selenium

Completar funções de teste no main.py

Executar testes com Pytest

📂 Arquivos do Sprint 8

main.py – funções de teste principais:

class TestUrbanRoutes:
    @classmethod
    def setup_class(cls):
        if helpers.is_url_reachable(data.URBAN_ROUTES_URL):
            print("Conectado ao servidor Urban Routes")
        else:
            print("Não foi possível conectar ao Urban Routes. Verifique o servidor")

    @classmethod
    def teardown_class(cls):
        print("Finalizando execução dos testes Urban Routes")

    def test_set_route(self): ...
    def test_select_plan(self): ...
    def test_fill_phone_number(self): ...
    def test_fill_card(self): ...
    def test_comment_for_driver(self): ...
    def test_order_blanket_and_handkerchiefs(self): ...
    def test_order_2_ice_creams(self): ...
    def test_car_search_model_appears(self): ...


pages.py – classe POM:

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


✅ Conclusão
Sprint 8 concluído: testes do Urban Routes totalmente automatizados, preparados para execução com Pytest. 🚀

🔗 Repositório: fcalvess-QA-Brazil_Python_Automation
