Sprint 7 — Introdução à Automação de Testes 🤖🧪

📝 Descrição do Sprint
Neste sprint, iniciamos a automação de testes do Urban Routes com Python. O objetivo é preparar funções, variáveis e arquivos para implementar os testes reais com Selenium no Sprint 8.

🎯 Objetivos do Sprint

Criar arquivos auxiliares (helpers.py, data.py)

Adicionar constantes de dados de teste

Criar funções de teste vazias em main.py

Preparar verificação de servidor Urban Routes

Preparar estrutura para testes futuros com Selenium

📂 Arquivos do Sprint 7

helpers.py – código auxiliar fornecido (não modificar)

data.py – constantes de dados de teste:

URBAN_ROUTES_URL = ''

ADDRESS_FROM = 'East 2nd Street, 601'
ADDRESS_TO = '1300 1st St'
PHONE_NUMBER = '+1 123 123 12 12'
CARD_NUMBER = '1234 5678 9100'
CARD_CODE = '1111'
MESSAGE_FOR_DRIVER = 'Pare no bar de sucos'


main.py – classe TestUrbanRoutes com funções de teste vazias:

class TestUrbanRoutes:
    @classmethod
    def setup_class(cls):
        if helpers.is_url_reachable(data.URBAN_ROUTES_URL):
            print("Conectado ao servidor Urban Routes")
        else:
            print("Não foi possível conectar ao Urban Routes. Verifique se o servidor está ligado e ainda em execução.")

    def test_set_route(self):
        #Adicionar em S8
        pass

    def test_select_plan(self):
        #Adicionar em S8
        pass

    def test_fill_phone_number(self):
        #Adicionar em S8
        pass

    def test_fill_card(self):
        #Adicionar em S8
        pass

    def test_comment_for_driver(self):
        #Adicionar em S8
        pass

    def test_order_blanket_and_handkerchiefs(self):
        #Adicionar em S8
        pass

    def test_order_2_ice_creams(self):
        for _ in range(2):
            #Adicionar em S8
            pass

    def test_car_search_model_appears(self):
        #Adicionar em S8
        pass


✅ Conclusão
Sprint 7 concluído com arquivos, constantes e funções prontas para o Sprint 8. 🚀
Repositório usado: QA-Brazil_Python_Automation
