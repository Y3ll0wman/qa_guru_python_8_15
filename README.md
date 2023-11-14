# Проект по тестированию сайта "Saber Interactive"
> <a target="_blank" href="https://cyber.games/">Saber Interactive</a>

![main page screenshot](/qa_guru_python_8_15/pictures/main_page.jpg)

### Список проверок, реализованных в автотестах

- [x] Раздел 'About' отображается
- [x] Перейти к игровому проекту возможно
- [x] Перейти к студии возможно
- [x] Перейти к новости возможно
- [x] Перейти в раздел 'Careers' возможно
- [x] Отправить контакты возможно

[//]: # (### Тест-кейсы)

[//]: # ()
[//]: # (![main page screenshot]&#40;/qa_guru_python_8_15/pictures/test-case-mind-map.png&#41;)

### Используемый стэк

<img title="Python" src="qa_guru_python_8_15/pictures/icons/python-original.svg" height="40" width="40"/> <img title="Pytest" src="qa_guru_python_8_15/pictures/icons/pytest-original.svg" height="40" width="40"/> <img title="Jira" src="qa_guru_python_8_15/pictures/icons/jira-original.svg" height="40" width="40"/> <img title="Allure Report" src="qa_guru_python_8_15/pictures/icons/Allure_Report.png" height="40" width="40"/> <img title="Allure TestOps" src="qa_guru_python_8_15/pictures/icons/AllureTestOps.png" height="40" width="40"/> <img title="GitHub" src="qa_guru_python_8_15/pictures/icons/github-original.svg" height="40" width="40"/> <img title="Selenoid" src="qa_guru_python_8_15/pictures/icons/selenoid.png" height="40" width="40"/> <img title="Selenium" src="qa_guru_python_8_15/pictures/icons/selenium-original.svg" height="40" width="40"/> <img title="Selene" src="qa_guru_python_8_15/pictures/icons/selene.png" height="40" width="40"/> <img title="Pycharm" src="qa_guru_python_8_15/pictures/icons/pycharm.png" height="40" width="40"/> <img title="Telegram" src="qa_guru_python_8_15/pictures/icons/tg.png" height="40" width="40"/>

### Локальный запуск автотестов

#### Выполнить в cli:
```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
pytest . --browser-version=100
```

#### Получение отчёта:
```bash
allure serve build/allure-results
```

### Запуск автотестов в Jenkins
> <a target="_blank" href="https://jenkins.autotests.cloud/job/Saber-Interactive-Auto-Tests/">Ссылка на проект в Jenkins</a>

#### Параметры сборки
> [!WARNING]
> Critical content demanding immediate user attention due to potential risks.
```python
BROWSER_VERSION = 100 # Версия браузера
ENVIRONMENT = ['STAGE', 'PREPROD', 'PROD']
COMMENT = 'some comment'
```

#### 1. Открыть <a target="_blank" href="https://jenkins.autotests.cloud/job/Saber-Interactive-Auto-Tests/">проект</a>

![jenkins project main page](qa_guru_python_8_15/pictures/jenkins_project_main_page.png)

#### 2. Нажать "Build with Parameters"
#### 3. В поле "BROWSER_VERSION" ввести: 100
#### 4. Из списка "ENVIRONMENT" выбрать: PROD
#### 5. В поле "COMMENT" ввести комментарий
#### 6. Нажать "Build"

![jenkins_build](qa_guru_python_8_15/pictures/jenkins_build.png)