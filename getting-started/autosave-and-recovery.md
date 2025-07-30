---
icon: light-emergency-on
---

# Autosave and Recovery

## Autosave Menu

The Autosave feature in Gaea is a crucial tool designed to automatically save your project at regular intervals. This ensures that your work is periodically backed up, minimizing data loss in the event of unexpected software shutdowns or system failures.

<figure><img src="../.gitbook/assets/image (38).png" alt="" width="375"><figcaption></figcaption></figure>

**Remind Me to Save Every.** This option allows you to set the frequency of the Autosave reminders. You can choose from the following intervals **5 minutes, 10 minutes, 15 minutes, 30 minutes.**

{% hint style="warning" %}
Selecting one of these options will configure the application to remind you to save your work at the chosen interval. Gaea autosaves every 10 minutes by default, and saves a Disaster Recovery file every 5 seconds (see [#disaster-recovery](autosave-and-recovery.md#disaster-recovery "mention"))
{% endhint %}

**Reset Timer.** Selecting 'Reset Timer' will restart the countdown of the current Autosave interval. This is useful when you want to make sure that a save happens at a specific point during your work session.

#### Revert Options

**Revert to.** Under this sub-menu, you can find a list of the most recent Autosave points. Each entry is labeled with a sequential number and the time of the save (e.g., Autosave 4 @ 03:16:46). This feature allows you to revert your project to a previous state, which is extremely helpful if you need to go back to an earlier version of your work due to errors or changes that did not produce the desired outcome.

**Autosave Entry.** The 'Autosave Entry' option at the bottom of the 'Revert to' list represents the initial state of your project when the Autosave feature was first enabled.

**Revert to Saved.** The 'Revert to Saved' button allows you to quickly revert your project to the last manually saved state. This is used to discard any changes made after the last manual save if they are no longer needed or desired.

### Usage Tips

* **Regular Saves**: In addition to relying on Autosave, regularly save your work manually to capture significant changes.
* **Adjust Frequency**: Adjust the Autosave frequency based on the complexity and duration of your tasks. More frequent saves are recommended for larger, more complex projects.
* **Check Autosave Files**: Periodically check the Autosave files to confirm they are being created as expected. This verification helps to avoid potential data loss.

***

## Disaster Recovery

Sometimes your Gaea instance might crash, or a hardware failure may cause your computer to crash or reboot. Gaea uses a background thread to save your latest action every 5 seconds.

In your [Gaea Data Folder](install-gaea/) you will find a `\Autosaves\recovery.terrain` file.

{% hint style="danger" %}
It is important to check both the `recovery` and `autosave` files which are also in the same folder. If the 5-second-time that saves recovery information has not fired before the crash, then you may need to use the most recent autosave as the latest recovery file may not have saved. This does not happen often, but it is a possibility.
{% endhint %}

### Version Migration Backup

When Gaea opens a file saved in an older version, it will save a copy of the original in the Autosave folder with the name convention: `Migration_<originalName>.terrain`

If a new version is not backward compatible, you can use such migration copies to recover older data in a disaster scenario.
