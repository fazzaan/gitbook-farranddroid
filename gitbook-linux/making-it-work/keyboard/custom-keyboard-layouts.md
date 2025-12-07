# Custom keyboard layouts

This isn't actually a problem for me yet — I am under the impression that it's pretty each to make a keyboard layout. I just haven't tried doing it yet.



There's projects to convert Microsoft Keyboard Layout Creator (MSKLC) `.klc` files into `.xkb` format, but there are issues with this.

One issue is "ligatures" (not really ligatures) — when you want to send 2 or more characters with one keypress. Microsoft's MSKLC is able to send two chars maximum, but xkb actually cannot. The project I used to convert the file _does_ produce an XCompose file, which is supposed to handle the "ligatures", but it doesn't work and idk why. The developer for this project has written very little documentation.

Anyway, the conversion worked, and the project also creates "installation" scripts which add the xkb keyboard layout file to your operating system and also update an xml listing somewhere else in the system.

The project is here:

{% tabs %}
{% tab title="Keyboard Layout Converter" %}
😸 GitHub here — [github.com/39aldo39/klfc](https://github.com/39aldo39/klfc)&#x20;
{% endtab %}
{% endtabs %}

