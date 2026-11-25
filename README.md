# My Marstek

A small app that watches a **Marstek Venus** home battery over your local network: is the power on,
how much charge is left, how long the battery will last, and a history of power outages.
It lives in the menu bar, shows a desktop widget and sends notifications (and, optionally, Telegram messages)
when the power goes out or comes back.

*Українською — нижче.*

## Downloads

Releases for each platform are tagged separately:

- **Mac** — tags `mac-v…`, file `MyMarstek-<version>-mac.zip`
- **Windows** — tags `windows-v…`

Open [Releases](../../releases) and pick the latest one for your platform.

## Requirements

- macOS 14 Sonoma or newer (Apple silicon or Intel).
- A Marstek Venus battery on the same network as the Mac, with **Open API (Local API)** turned on
  in the Marstek app (default UDP port 30000).
- Built and tested with the **Venus E mini** in **UPS** mode with the house on the battery's backup outlet.
  Other Venus models speak the same protocol (charge, temperature, capacity work everywhere), but outage
  detection and house load assume that UPS setup.

## Installing on Mac

The app is free and not notarized by Apple, so macOS asks you to confirm it once:

1. Download `MyMarstek-<version>-mac.zip`, unzip it and move **My Marstek** to **Applications**.
2. Open it. macOS will say it can't check the app — click **Done**.
3. Open **System Settings → Privacy & Security**, scroll down and click **Open Anyway** next to My Marstek.
4. Allow **Local Network** access when asked — the app needs it to talk to the battery.

On first launch the app looks for the battery on your network by itself. If it finds none,
enter the battery's IP address in Settings.

## Updating

Once a day the app checks this page. When a new version is out, a **New version** badge appears in the
main window (and in Settings → App). Download the new zip and replace the app in Applications —
your settings and history are kept. If you use Telegram, macOS may ask once to let the new version
read the bot token from the keychain.

## Privacy

Everything stays on your Mac: the app talks only to the battery (and a Matter smart socket, if you add one)
on your local network. The only internet requests are the daily update check to GitHub and, if you turn it
on, your own Telegram bot.

---

# My Marstek (українською)

Невеликий застосунок, що стежить за домашньою батареєю **Marstek Venus** через локальну мережу: чи є світло,
скільки лишилося заряду, на скільки вистачить батареї, історія відключень. Живе в рядку меню, має віджет
і надсилає сповіщення (за бажанням — у Telegram), коли світло зникає або повертається.

## Завантаження

Релізи для Mac мають теги `mac-v…` (файл `MyMarstek-<версія>-mac.zip`), для Windows — `windows-v…`.
Відкрийте [Releases](../../releases) і виберіть останній для своєї системи.

## Вимоги

- macOS 14 Sonoma або новіша.
- Батарея Marstek Venus у тій самій мережі, що й Mac, з увімкненим **Open API (Local API)** у застосунку
  Marstek (UDP-порт 30000 за замовчуванням).
- Перевірено на **Venus E mini** у режимі **UPS**, коли дім підключено до резервної розетки станції.
  Інші моделі Venus мають той самий протокол, але визначення відключень і навантаження розраховані на таку схему.

## Встановлення на Mac

Застосунок безкоштовний і не нотаризований Apple, тож macOS попросить підтвердження один раз:

1. Завантажте `MyMarstek-<версія>-mac.zip`, розпакуйте й перенесіть **My Marstek** у **Програми**.
2. Відкрийте його. macOS скаже, що не може перевірити застосунок, — натисніть **Готово**.
3. Відкрийте **Системні параметри → Приватність і безпека**, прокрутіть униз і натисніть
   **Усе одно відкрити** біля My Marstek.
4. Дозвольте доступ до **локальної мережі** — без нього застосунок не бачить батарею.

Під час першого запуску застосунок сам шукає батарею в мережі. Якщо не знайде — введіть її IP-адресу в налаштуваннях.

## Оновлення

Раз на добу застосунок перевіряє цю сторінку. Коли виходить нова версія, у головному вікні з'являється
плашка **Нова версія** (і в Налаштування → Застосунок). Завантажте новий архів і замініть застосунок
у Програмах — налаштування та історія збережуться.

## Приватність

Усе залишається на вашому Mac: застосунок спілкується лише з батареєю (і розеткою Matter, якщо ви її додали)
у локальній мережі. В інтернет іде тільки щоденна перевірка оновлень на GitHub і, якщо ви його ввімкнете,
ваш власний Telegram-бот.
