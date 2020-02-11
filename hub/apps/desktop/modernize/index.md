---
Description: Add modern XAML user interfaces, create MSIX packages, and incorporate other modern components into your desktop application.
title: Modernize your desktop apps for Windows
ms.topic: article
ms.date: 04/17/2019
ms.author: mcleans
author: mcleanbyron
ms.localizationpriority: medium
---

# Modernize your desktop applications

Windows 10 and the Universal Windows Platform (UWP) offer many features you can use to deliver a modern experience in your desktop apps. Most of these features are available as modular components that you can adopt in your desktop apps at your own pace without having to rewrite your application for a different platform. You can enhance your existing desktop apps by choosing which parts of Windows 10 and UWP to adopt.

This article describes the Windows 10 and UWP features that you can use in your desktop apps today. For a tutorial that demonstrates how to modernize an existing app to use many of the features described in this article, see the [Modernize a WPF app](modernize-wpf-tutorial.md) tutorial.

> [!NOTE]
> Do you need assistance migrating desktop apps to Windows 10? The [Desktop App Assure](https://docs.microsoft.com/FastTrack/win-10-desktop-app-assure) service provides direct, no-cost support to developers who are porting their apps to Windows 10. This program is available to all ISVs and eligible enterprises. For more details on eligibility and about the program itself, visit [https://aka.ms/DesktopAppAssure](https://aka.ms/DesktopAppAssure). To get started now, [submit your request](https://aka.ms/DesktopAppAssureRequest).

## MSIX packages

MSIX is a modern Windows app package format that provides a universal packaging experience for all Windows apps, including UWP, WPF, Windows Forms and Win32 apps. MSIX brings together the best aspects of MSI, .appx, App-V and ClickOnce installation technologies to provide a modern and reliable packaging experience.

Packaging your desktop Windows apps in MSIX packages gets you access to a robust installation and updating experience, a managed security model with a flexible capability system, support for the Microsoft Store, enterprise management, and many custom distribution models.

For more information, see [Package desktop applications](/windows/msix/desktop/desktop-to-uwp-root) in the MSIX documentation.

## .NET Core 3

.NET Core 3 is the latest major release of .NET Core. The highlight of this release is support for Windows desktop apps, including Windows Forms and WPF apps. You can run new and existing Windows desktop apps on .NET Core 3 and enjoy all the benefits that .NET Core has to offer. UWP controls that are hosted in [XAML Islands](xaml-islands.md) can also be used in Windows Forms and WPF apps that target .NET Core 3.

For more information, see [What's new in .NET Core 3.0](https://docs.microsoft.com/dotnet/core/whats-new/dotnet-core-3-0).

## UWP APIs

You can call many UWP APIs directly in your WPF, Windows Forms, or C++ Win32 desktop app to integrate modern experiences that light up for Windows 10 users. For example, you can call UWP APIs to add toast notifications to your desktop app.

For more information, see [Use UWP APIs in desktop apps](desktop-to-uwp-enhance.md).

## Host UWP controls (XAML Islands)

Starting with the Windows 10, version 1903, you can add [UWP XAML controls](/windows/uwp/design/controls-and-patterns/controls-by-function) directly to any UI element in a WPF, Windows Forms, or C++ Win32 app that is associated with a window handle (HWND). This means that you can fully integrate the latest UWP features such as [Windows Ink](/windows/uwp/design/input/pen-and-stylus-interactions) and controls that support the [Fluent Design System](/windows/uwp/design/fluent-design-system/index) into windows and other display surfaces in your desktop apps. This developer scenario is sometimes called *XAML islands*.

For more information, see [UWP controls in desktop apps](xaml-islands.md)

## Use the Visual layer in desktop apps

You can now use UWP APIs in non-UWP desktop apps to enhance the look, feel, and functionality of your WPF, Windows Forms, and C++ Win32 apps, and take advantage of the latest Windows 10 UI features that are only available via UWP. This is useful when you need to create custom experiences that go beyond the built-in UWP controls you can host by using XAML Islands.

For more information, see [Modernize your desktop app using the Visual layer](visual-layer-in-desktop-apps.md).

## Additional features available to apps with package identity

Some modern Windows 10 experiences are available only in desktop apps that have [package identity](https://docs.microsoft.com/uwp/schemas/appxpackage/uapmanifestschema/element-identity). These features include certain UWP APIs, package extensions, and UWP components. For more information, see [Features that require package identity](modernize-packaged-apps.md).

There are several ways to grant identity to a desktop app:

* Package it in an [MSIX package](/windows/msix/desktop/desktop-to-uwp-root). MSIX is a modern app package format that provides a universal packaging experience for all Windows apps, WPF, Windows Forms and Win32 apps. It provides a robust installation and updating experience, a managed security model with a flexible capability system, support for the Microsoft Store, enterprise management, and many custom distribution models. For more information, see [Package desktop applications](https://docs.microsoft.com/windows/msix/desktop/desktop-to-uwp-root) in the MSIX documentation.
* If you are unable to adopt MSIX packaging for deploying your desktop app, starting in Windows 10 Insider Preview Build 10.0.19000.0 you can grant package identity by creating a *sparse MSIX package* that contains only a package manifest. For more information, see [Grant identity to non-packaged desktop apps](grant-identity-to-nonpackaged-apps.md).

<a id="desktop-uwp-controls"/>

## UWP controls optimized for desktop apps

Whether you're building a UWP app that exclusively targets the desktop device family or you want to use UWP controls in a WPF, Windows Forms, or C++ Win32 desktop app, the following new and updated UWP controls are designed to offer desktop-optimized experiences with the [Fluent Design System](/windows/uwp/design/fluent-design-system/index). These controls were introduced in Windows 10, version 1809 (the October 2018 Update, or version 10.0.17763).

| Control |  Description |
|------ |--------------|
| [MenuBar](https://docs.microsoft.com/windows/uwp/design/controls-and-patterns/menus#create-a-menu-bar) | Provides a quick and simple way to expose a set of commands for apps that might need more organization or grouping then a **CommandBar** allows. |
| [DropDownButton](https://docs.microsoft.com/windows/uwp/design/controls-and-patterns/buttons#create-a-drop-down-button) | Shows a chevron as a visual indicator that it has an attached flyout that contains more options.  |
| [SplitButton](https://docs.microsoft.com/windows/uwp/design/controls-and-patterns/buttons#create-a-split-button) | Provides a button has two parts that can be invoked separately. One part behaves like a standard button and invokes an immediate action. The other part invokes a flyout that contains additional options that the user can choose from.|
| [ToggleSplitButton](https://docs.microsoft.com/windows/uwp/design/controls-and-patterns/buttons#create-a-toggle-split-button) | Provides a button has two parts that can be invoked separately. One part behaves like a toggle button that can be on or off. The other part invokes a flyout that contains additional options that the user can choose from. |
| [CommandBarFlyout](https://docs.microsoft.com/windows/uwp/design/controls-and-patterns/command-bar-flyout) |  Lets you show common user tasks in the context of an item on your UI canvas. |
| [ComboBox](https://docs.microsoft.com/windows/uwp/design/controls-and-patterns/combo-box#make-a-combo-box-editable) | You can now make a combo box editable so the user can enter values that aren't listed in the control.  |
| [TreeView](https://docs.microsoft.com/windows/uwp/design/controls-and-patterns/tree-view) | You can now configure a tree view to enable data binding, item templates, and drag and drop.  |
| [DataGridView](https://docs.microsoft.com/windows/communitytoolkit/controls/datagrid) |   Provides a flexible way to display a collection of data in rows and columns. This control is available in the [Windows Community Toolkit](https://docs.microsoft.com/windows/uwpcommunitytoolkit/).  |

## Windows UI Library

The Windows UI Library is a set of NuGet packages that provide new controls and other user interface elements for UWP apps. Windows UI Library APIs work on earlier versions of Windows 10, so your app works even if users aren't running the latest version of Windows 10. This lets you adopt new controls as they are released in the Windows UI Library without having to worry about including version checks or conditional XAML.

See [Windows UI Library](https://docs.microsoft.com/uwp/toolkits/winui/).

## Other technologies for modern desktop apps

### Microsoft Graph

Microsoft Graph is a collection of APIs you can use to build apps for organizations and consumers that interact with the data of millions of users. Microsoft Graph exposes REST APIs and client libraries to access data on the following:
* Azure Active Directory
* Office 365 services: SharePoint, OneDrive, Outlook/Exchange, Microsoft Teams, OneNote, Planner, and Excel
* Enterprise Mobility and Security services: Identity Manager, Intune, Advanced Threat Analytics, and Advanced Threat Protection.
* Windows 10 services: activities and devices

For more information, see the [Microsoft Graph docs](https://developer.microsoft.com/graph/docs/concepts/overview).

### Adaptive Cards

Adaptive Cards is an open, cross-platform framework that you can use to exchange card-based UI content in a common and consistent way across devices and platforms.

For more information, see the [Adaptive Cards docs](https://docs.microsoft.com/adaptive-cards/).
