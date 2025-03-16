---
title: \block
page_title: \block
description: The \block command.
show_outline: false
category: Main
nav_order: 3
mentions:
    - stormstqr
---

Manages blocks.

<CommandDetailsTable
    name="\block"
    :categories="[
        'world', 'blocks'
    ]"
    :requiredTags="[
        'canUseChatCommands'
    ]"
    ultraSecurityModeSecurityLevel="admin"
    version="0.2.7-alpha.36"
    :undoSupported="-1"
    :functional="true"
    :deprecated="false"
/>

## Syntax

`\block`{lang=andexdbcmd}

<indent></indent>

`\block facing get color ...`{lang=andexdbcmd}

-   `... <colorSpace: rgba|rgb> <unit: hex|frac|dec|decr>`{lang=andexdbcmd}

-   `... <colorSpace: hsl|hsluv|(hsv|hsb)|hsi|hpluv|AdobeRGB|CIELuv|CIExyY>`{lang=andexdbcmd}

`\block facing get filllevel`{lang=andexdbcmd}

<indent></indent>

`\block facing set color ...`{lang=andexdbcmd}

<indent></indent>

`\block facing set filllevel <fillLevel: int[min=0,max=6]>`{lang=andexdbcmd}

<indent></indent>

## Result

<template-EmptySection />

## History

<template-EmptySection />
