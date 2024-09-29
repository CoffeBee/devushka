# Диспач работы
Вся наша работа в рамках дистуров будет оценина с точки зрения трудозатрат, цели такого подхода:

- Избежать неравномерного вклада преподавателей в процесс
- Объективно оценить объем новой для нас работы
- Прозрачно показывать динамику наших трудозатрат для функционирования кружка

В качестве единой меры было выбрано ```30мин работы``` = ```найти одну А муниципа``` = ```1TP```

В течение года ведется подчет потраченого для подготовки дистуров времени каждым из людей, выраженный в TP-ах. Обозначим этот словарь как ```inpact```, тогда назначение очередной задачи в базовом случае (см. исключение в разделе "Поиск задач вне нужды") работает так:
```python
from random import radnint

def can_do(teacher):
    # the magical function that determines whether
    # the teacher can perform this job
    return secret_predicate

teachers.sort(
    key=lambda teacher: (
        impact[teacher],
        randint(1, 1337),
    )
)

for teacher in teachers:
    if can_do(teacher):
        print(f"Работу выполнет {teacher}!")
        exit(0)
print("Пиздец")
```

В магической функции ```can_do``` внесены ограничения на выполнение работы, требующей высокий уровень достижений в олимпиадах. Каждый из людей знает эти ограничения только лишь про себя.

Суммарные трудозатраты команды на дистуры в неделю расчитаны как ```24TP``` = ```10 человек часов``` ~ ```35 минут на человека```.

При этом лишь ```16.5TP``` из ```24TP``` являются базовой частью (которая в любом случае должна быть выполнена), а оставшиеся ```7.5TP``` могут быть использованы для доразработки задач для которых нет полного архива.

# Требования
### Поиск задачи
Основной формат работы, присутствующий в разработке дистуров. 

#### Про муницип
Если вам выпала задача муниципального этапа, пожалуйста, ориентируйтесь на уровень сложности **московского** муниципа.

Примерный список тем, которые можно освещать на каждой из позиций муниципа:
| Задача    | Темы |
| -------- | ------- |
| Муницип A  | Формулы   |
| Муницип В | Формулы, простой бинпоиск,<br> конструктивы     |
| Муницип C / Регион А    | Формулы, бинпоиск,<br> жадности, конструктивы, <br>префиксные суммы    |
| Муницип D | бинпоиск,конструктивы, <br> жадности, префиксные суммы    |
| Муницип E / Регион B    | бинпоиск,конструктивы, <br> жадности, префиксные суммы,<br> линейные алгоритмы, сканлайн, <br> динамика, BFS/DFS    |

#### Архивы задач
Мы не выстанавливаем единные ограничения на пулл используемых источников, но мы руководствуемся некоторыми правилами:

- Не используем те задачи, что встречались последние два года на дистурах Яндекс (ex. Тинькофф)
- Стараемся неиспользовать задачи, которые были последние года на московских сборах. Технически это не возможно определить точно, но мы воздерживаемся от использования архивов COCI и белорусской олимпиады
- используем рекомендованные архивы: [KOI](https://koi.or.kr), [BOI](https://boi.cses.fi/contests.php), [Японские олимпиады](https://www2.ioi-jp.org/joi/2017/2018-ho/index.html), [USACO](https://usaco.org/index.php?page=history), [GEOI](https://geoi.ge), [УкрОИ](https://io.in.ua), [контесты с baekjoon](https://acmicpc.net) и другие

#### Ревью задачи
После того как вы нашли задачу и выполнили в полном объеме все пункты описаные ниже, вашу задачу смотрет ревьювер.
В первую очередь вы от него получаете фидбек подходит ли эта задача на ту позицию, что вы делаете, а также в успешном случае выставляет оценку по шкале нормально-хорошо-отлично. Если задача не подходит вам нужно найти другую.
Во вторую очередь ревьювер проверяет техническое качество задачи, аспекты найденные на этой фазе тоже должны быть исправлены.
[Подробнее про ревью](http://dev.algocourses.ru/guide/review)

#### Порядок работы
В качестве вводных вы получаете позицию, под которую вы ищите задачу
В качестве результата вы должны предоставить:

1. Ссылку на оригинал задачи
2. Ссылку на задачу в полигоне
2.1 В этой задаче должно быть полное переведенное на русский условие задачи
2.1 Если в задаче присутсвуют в каком либо виде тесты для каждой из подгрупп, то в полигоне также появится залитые, размеченные тесты, чекер и авторское решение.
2.2 Если в задаче отсутсвуют тесты, вы должны завести задачу на их разработку, сделать это можно только если суть задачи получила оценку отлично, также должны на этой недел еще оставаться [ресурсы команды](http://dev.algocourses.ru/guide/dispatch). Если задачу на разработку тестов завести нельзя, нужно искать другую задачу.
3. Список тем используемых в решение задачи на 100 баллов.

#### Оценка трудозатрат
Базовая оценка в зависимости от позиции
| Задача    | Оценка |
| -------- | ------- |
| Муницип A  | 1TP   |
| Муницип В | 1TP     |
| Муницип C / Регион А    | 1.5TP   |
| Муницип D | 1.5TP    |
| Муницип E / Регион B    | 1.5TP    |
| Регион C | 2TP    |
| Регион D    | 2.5TP    |

Также в зависимости от различных ситуаций при заливке начисляются бонусы
| Ситуация    | Бонус |
| -------- | ------- |
| Нет разметки на группы | 10% стоимости задачи   |
| Нет авторского | 20% стоимости задачи     |
| Отсутствует кастомный чекер    | 0.75TP   |

Эта работа выполняется до 23:59-UTC+3/MSC среды.

#### Поиск задач вне нужды
Если в процессе поиска нужной вам задачи вы встретили хорошую задачу на другую позицию, вы можете предложить её на рассмотрение. Ваша задача будет рассмотрена ревьювером, и в случае успеха она будет добавлена в очередь на позицию.

При последующих назначениях, если в очереди есть задачи на одну из позиций, диспач на эту позицию происходить не будет; просто будет взята первая задача из очереди, а её автору будут записаны TP.

### Ревью
Глобально главная цель ревью состоит в удержание качества задач, которые мы выдаем детям на дистуры.

Первая фаза ревью задачи состоит из оценки ее сути, тут вы должны выбрать один из 4 вариантов:
1. Задача не подходит, мы неготовы ее дать на дистур. В этом случае нужно доходчево описать почему задача не подходит, сославший на один из вариантов: слишком простая/сложная, баян, слишком учебная или не подходящий формат. **Нормально**.
2. Задача подходит на свою позицию, но задача скучная или звучит искуствено.
3. Задача звучит так, что ее можно было бы дать на соответствующую олимпиаду, но ее бы не назвали лучшей задачей тура. **Хорошо**.
4. Задача была бы достойна стать лучшей задачей тура на настоящей олимпиаде. **Отлично**.

Учитывайте, что ставя оценку отлично, вы допускаете ситуацию, что команда потратит ресурс на разработку тестов.

Второй фазой ревью является валидация:

- верности перевода
- правильности выбранного чекера
- валидности тестов
- одыкватности источника решения
- компилируемость всех элементов задачи

Также вы должны составить список тем используемых в решение задачи на 100 баллов.

Трудозатратностью ревью расчитывается как 50% стоимости задачи.

Это работа выполняется в течение 48 часов после получения запроса от человека делавшего задаачу, но не позже 16:00-UTC+3/MSC пятницы.

### Разработка тестов
Если в задаче, которую мы очень хотим взять, не нашлось тестов, или тесты есть только для полной подгруппы, то при наличие ресурса, мы можем взять эту задачу в разработку.
Дедлайн на появляние запроса на разработку 23:59-UTC+3/MSC четверга.

Разработка оценивается в каждом случае индивидуально, но неможет быть оценина выше чем 150% от стоимости поиска задачи.

Согласовать разработку могут только: Ваня Подворный, Саша Горнак и Саша Бабин.