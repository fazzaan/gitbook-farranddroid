# During video calls

One reason could be the over-usage of the CPU, causing the clock speed to be limited.

On my lightweight, low-powered laptop, the CPU automatically limits its power and clock speed when most of the cores are in use.

Video calling in the web browser uses a feature called WebRTC, and this typically uses as many CPU cores as it can.

This inevitably leads to the CPU speed being limited, and the laptop becomes unusable.

## Apps which cause this

(In my experience)

* Video calling in a web browser, especially [Chromium browsers](#user-content-fn-1)[^1]&#x20;
* Telegram desktop app (may have improved recently; I haven't tested it for a few months)&#x20;

## Solutions

There are a couple of solutions to this.

1. Limit the number of CPU cores that the offending process/es have access to.&#x20;
2. Limit the CPU utilization percentage that the offending process/es have access to.&#x20;
3. Raise the CPU rate-limiting threshold/s.&#x20;





[^1]: Chrome, Edge, Brave, Opera, etc.
