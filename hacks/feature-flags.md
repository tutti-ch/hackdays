---
hackname: feature-flags
quicksummary: deploy != release
resource: true
archived: false
award: top
categories: [hack]
---

# Tutti Feature Flags FTW!

The goal of the hack to provide a small react component POC that demo one of the ways how we may use feature flags at Tutti.

## Do we need this hack?

Answer the following questions, in order to determine,
if this project is needed for your team.

Can my team…
* apply [Dark Launching](https://github.com/adamluzsi/toggler/blob/master/docs/DarkLaunch.md) practices ?
* deploy frequently the codebase independently from feature release ?
* perform deployment during normal business hours with negligible downtime ?
* release feature without needing fine-grained communication and coordination with people outside of the team ?
* deploy and release its product or service on demand, independently of other services the product or service depend upon ?
* try out feature on the active userbase incrementally ?

If your answer yes to most of them, then you should check out the other hacks since the goal is achieved then.
else, please continue...

## Planned Features

### Rollout management

The service allows you to be able to control feature release, trough a combination of options.

### Manual rollout

The basic scenario where you can enroll users to become a pilot of a new feature,
that you want to measure trough they feedback and usage.
This is useful when you have loyal customers, who love to try out new features early,
and give feedback they personal feedback about it.

### Rollout By Percentage

This option is to enroll users based or percentage.
This happens when a feature flag status is being asked from the service.
If the currently calling User is win a Pseudo random lottery,
then the user is enrolled to become a pilot of the new feature.
The Pseudo random lottery allow the system to have deterministic
and reproducible rollout enrollment result for each pilot ID,
while ensuring that the user pool size can be infinitely big
without having any resource hit on the feature flag service.

Also this grant random like percentage based feature release distribution.
The randomness can be controlled by modifying the feature flag rollout random seed.
While you can manually enroll or blacklist users for piloting a feature,
that approach need to persist this information.
This on the other hand only rely on the fact that the external id for the user is uniq on system level.
The users that lost in the enrollment can still be enrolled when the rollout percentage increase.

#### Global Release

In some cases you don't have such information as individual account ids.
Such scenario can be batch jobs behavior change feature releases.
In those cases, global state check for a given flag can be used.

#### A/B Testing

When it is unknown what will be more suitable for the users,
it is a common practice to test two version on a small subset of the userbase,
and monitor the results closely from the users.
If one of the version turns out to be success,
then it can be released for wider audience.

#### Experiments

Sometimes it is a requirement, to release a feature for certain target groups first,
for various reasons for the business.
For this it is a common practice to use target groups or "experiments".
It is a goal to provide the ability to create feature releases that can be decided based on our custom domain needs.

## Who's Participating?

- [Adam Luzsi](/hackdays/whoami/adamluzsi)
