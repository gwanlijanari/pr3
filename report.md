1 запуск (зеленый) https://github.com/gwanlijanari/pr3/actions/runs/41200828460
2 запуск после изменения стиля (красный) https://github.com/gwanlijanari/pr3/actions/runs/41201920068
3 запуск после исправления (зеленый) https://github.com/gwanlijanari/pr3/actions/runs/41202121805
4 запуск после изменения комнаты (зеленый) https://github.com/gwanlijanari/pr3/actions/runs/41202367751

прогноз - чекап-билд сломается. он сломался


упавший тест:
Run python -m unittest discover -s tests -v
test_heading (test_site.SiteTests.test_heading) ... ok
test_lesson_topic (test_site.SiteTests.test_lesson_topic) ... ok
test_stylesheet_exists (test_site.SiteTests.test_stylesheet_exists) ... 
  test_stylesheet_exists (test_site.SiteTests.test_stylesheet_exists) (href='missing.css') ... FAIL
test_title (test_site.SiteTests.test_title) ... ok

======================================================================
FAIL: test_stylesheet_exists (test_site.SiteTests.test_stylesheet_exists) (href='missing.css')
----------------------------------------------------------------------
Traceback (most recent call last):
  File "/home/runner/work/pr3/pr3/tests/test_site.py", line 54, in test_stylesheet_exists
    self.assertTrue(bool(href) and (SITE / href).is_file(),
AssertionError: False is not true : Missing stylesheet: missing.css

----------------------------------------------------------------------
Ran 4 tests in 0.001s

FAILED (failures=1)
Error

шаги:
тест упал, экшн остановил работу, билд и сейв артефакт не сработали 

тесты выполнялись на удаленном сервере гитхаба

тесты проверяют не правильность данных а то что сам синтаксис верный
