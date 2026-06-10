# HIVE – Hyperlocal Boutique Fashion Marketplace

A full-stack hyperlocal fashion marketplace connecting customers with independent fashion boutiques through a modern multi-tenant platform.

HIVE enables customers to discover local boutique collections, place orders, track deliveries, and download invoices while providing dedicated management portals for boutique partners and marketplace administrators.

---

## Overview

HIVE is built as a marketplace ecosystem consisting of three independent applications:

### Customer Marketplace
A customer-facing shopping experience for discovering and purchasing boutique fashion products.

### Boutique Partner Portal
A seller dashboard that allows boutiques to manage products, inventory, and customer orders.

### Marketplace Administration Console
A centralized control panel for marketplace operations, boutique approvals, user management, and analytics.

---

## Key Features

### Customer Marketplace

#### Authentication & Profile Management
- Secure authentication using Clerk
- User profile management
- Session management

#### Product Discovery
- Homepage product discovery
- Global product search
- Category browsing
- Collection browsing
- Boutique discovery
- Product recommendations

#### Product Experience
- Product gallery
- Product details
- Boutique information
- Size selection
- Stock visibility
- Delivery information

#### Cart & Checkout
- Shopping cart management
- Address management
- Delivery scheduling
- Order summary
- Order placement

#### Order Management
- Order history
- Order tracking
- Real-time status updates
- Invoice downloads

#### Delivery Validation
- Radius-based serviceability checks
- Coordinate-based location validation
- Browse Products Anyway mode for non-serviceable locations

---

### Boutique Partner Portal

#### Boutique Management
- Boutique profile management
- Delivery radius configuration
- Store information management

#### Product Management
- Create products
- Edit products
- Delete products
- Manage product inventory
- Upload product media
- Manage product categories

#### Order Management
- View customer orders
- Update order status
- Track order progress
- Access order invoices

Supported order statuses:

- Confirmed
- Packed
- Out For Delivery
- Delivered

#### Business Dashboard
- Revenue metrics
- Order statistics
- Delivery insights
- Performance overview

---

### Marketplace Administration Console

#### User Management
- View platform users
- Role management
- User monitoring

#### Boutique Management
- Boutique approval workflow
- Boutique verification
- Boutique monitoring

#### Product Oversight
- Marketplace-wide product monitoring
- Product moderation

#### Category Management
- Create categories
- Edit categories
- Delete categories

#### Banner Management
- Homepage promotional banners
- Marketing content management

#### Order Monitoring
- View all marketplace orders
- Monitor delivery lifecycle
- Access invoices
- Customer and boutique details

#### Marketplace Analytics
- Revenue insights
- Order analytics
- Boutique metrics
- Platform statistics

---

# Order Lifecycle

Customer places order

↓

Order Created

↓

Boutique Receives Order

↓

Order Confirmed

↓

Order Packed

↓

Out For Delivery

↓

Delivered

↓

Invoice Available

---

# Invoice System

The platform automatically generates invoices for completed orders.

Invoices are accessible to:

- Customers
- Boutique Partners
- Marketplace Administrators

Invoice details include:

- Order Information
- Customer Information
- Boutique Information
- Product Breakdown
- Pricing Summary
- Delivery Information

---

# Email Notification System

Transactional email infrastructure powered by Resend.

### Customer Notifications
- Order Confirmed
- Order Packed
- Out For Delivery
- Order Delivered

### Boutique Notifications
- New Order Received
- Order Delivered Confirmation

---

# Delivery Intelligence

HIVE uses coordinate-based delivery validation.

Delivery eligibility is determined using:

- Customer coordinates
- Boutique coordinates
- Boutique delivery radius

This allows accurate hyperlocal delivery coverage without relying on city-based restrictions.

---

# Media Infrastructure

Cloudinary is integrated for:

- Product image storage
- Product video storage
- Boutique verification documents
- Customer claim evidence uploads
- CDN delivery
- Responsive image optimization
- Media transformations
- Video asset delivery

---

# Technology Stack

## Frontend

- Next.js
- React
- TypeScript
- Tailwind CSS
- ShadCN UI

## Backend

- Convex

## Authentication

- Clerk

## Database

- Convex Database

## Media Storage & Delivery

- Cloudinary

## Transactional Emails

- Resend

## Monorepo Architecture

- Turborepo

---

# Platform Architecture

text Customer Marketplace         │         ▼      Next.js         │         ▼       Convex         │  ┌──────┼────────┬─────────┐  ▼      ▼        ▼         ▼ Clerk Cloudinary Resend Database Auth   Media     Email   Storage 

---

# Security & Access Control

### Customers

Can:
- Browse products
- Place orders
- Track orders
- Download invoices

Cannot:
- Access boutique management
- Access admin controls

### Boutique Partners

Can:
- Manage own products
- Manage own orders
- Update order statuses

Cannot:
- Access admin controls
- Manage other boutiques

### Administrators

Can:
- Manage users
- Manage boutiques
- Manage categories
- Manage banners
- Monitor marketplace activity

---

# Project Structure

bash apps/ ├── customer/ ├── admin/  convex/ ├── orders.ts ├── products.ts ├── boutiques.ts ├── invoices.ts ├── emails.ts ├── users.ts  packages/ ├── ui/ ├── utils/ ├── types/ 

---

# APIs & Services

| Service | Purpose |
|----------|----------|
| Clerk | Authentication & User Management |
| Convex | Backend, Database & Real-Time Operations |
| Cloudinary | Media Storage & Delivery |
| Resend | Transactional Email Notifications |

---

# Highlights

- Multi-tenant marketplace architecture
- Customer, Boutique, and Admin applications
- Hyperlocal delivery validation engine
- Real-time order management system
- Automated invoice generation
- Responsive mobile-first design
- Cloud-based media infrastructure
- Transactional email notification system
- Role-based access control
- Scalable monorepo architecture
- End-to-end marketplace workflow

---

## Author

Yedukrishnan K R

HIVE was developed as a full-stack marketplace platform demonstrating modern web application architecture, real-time backend systems, hyperlocal commerce workflows, role-based access control, and scalable marketplace operations.
