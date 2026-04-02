# Cadence

Set how frequently each inherent risk tier should be re-assessed from **Settings → Cadence**.

| Risk Level   | Cadence       |
| ------------ | ------------- |
| **Critical** | Yearly        |
| **High**     | Every 2 years |
| **Medium**   | Every 3 years |
| **Low**      | No cadence    |

These are defaults — each tier can be adjusted independently using the dropdown.

Once a vendor's last assessment ages past the configured cadence, their lifecycle status updates to **Re-Assessment Required**, surfacing them in the inventory and on the Risk Dashboard's assessment hygiene gauge.

{% hint style="info" %}
Setting a tier to **No cadence** means vendors at that risk level will never be automatically flagged for re-assessment.
{% endhint %}
