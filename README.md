# Тренажёр для быстрого набора текста на клавиатуре(графическое приложение)

## Как взаимодействовать с приложением:
1) При запуске появится пользовательский интрефейс, в котором можно будет выбрать язык,
   которой хочется потренировать(изначально будут только русский и английский), затем кнопки
   старт и выход.
2) Нажав на кнопку старт, пользователь запускает таймер и ему выводится на экран текст, который
   нужно будет начать перепечатывать.
4) Во время печати система будет указывать пользователю на его ошибки.
5) После окончания таймера пользователь увидит свой результат - кол-во слов и кол-во ошибок.

## Функциональные элементы в коде:
1) Проект будет разбит на 2 класса - первый отвечает за логику приложения(генерит случайный текст
   либо использует текст пользователя, проверяет корректность набранного текста,
   включает и выключает таймер, подсчитывает кол-во слов и кол-во ошибок).
2) Второй класс будет отвечать за визуализацию пользовательского интерфейса: рисует нужные кнопки,
   выводит на экран время и результаты текущей печати.

\```
class user_interaction
  fields:
    words_count
    mistakes_count
    current_time
    current_text
  methods:
    set_text(text)
    generate_text(current_language) <- генирируется случайный текст на выбранном языке
    get_current_time()
    get_words_count()
    get_mistakes_count()
    play() <- в начале запускается таймер, и пока время не закончится, пользователь может вводить текст,
    за это время заполняются переменные words_count и mistakes_count.
\```

\```
class user_interface
  fields:
    window
    user_interaction
  methods:
    методы взаимодействия с кнопками
    dispaly()
\```
