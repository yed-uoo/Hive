# HIVE – Hyperlocal Boutique Fashion Marketplace

HIVE is a full-stack hyperlocal fashion marketplace platform that connects customers with independent fashion boutiques through a unified digital ecosystem.

The platform enables customers to discover boutique fashion, place orders, track deliveries, and access invoices, while providing dedicated management portals for boutique partners and marketplace administrators.

Built using a modern TypeScript-based monorepo architecture, HIVE demonstrates a complete marketplace workflow from product discovery to order fulfillment.

---

## Overview

HIVE is designed as a multi-tenant marketplace platform consisting of three independent applications:

### Customer Marketplace
A consumer-facing shopping platform for discovering and purchasing boutique fashion products.

### Boutique Partner Portal
A dedicated seller dashboard that enables boutiques to manage products, orders, inventory, and business operations.

### Marketplace Administration Console
A centralized management system for marketplace operations, boutique onboarding, user administration, and platform monitoring.

---

# Core Features

## Customer Marketplace

### Authentication & Account Management
- Secure authentication using Clerk
- User registration and login
- Session management
- Customer profile management

### Product Discovery
- Homepage product discovery
- Global marketplace search
- Category browsing
- Collection browsing
- Boutique discovery
- Product recommendations

### Product Experience
- Product galleries
- Detailed product information
- Boutique information
- Size selection
- Delivery information
- Product media support

### Cart & Checkout
- Shopping cart management
- Quantity management
- Address management
- Delivery slot selection
- Order placement

### Order Management
- Order history
- Order tracking
- Status timeline
- Invoice downloads

### Delivery Validation
- Hyperlocal serviceability validation
- Radius-based delivery checks
- Coordinate-based location verification
- Browse Products Anyway mode

---

## Boutique Partner Portal

### Boutique Management
- Boutique profile management
- Store information updates
- Delivery radius configuration

### Product Management
- Create products
- Edit products
- Delete products
- Upload product images
- Manage inventory
- Category assignment

### Order Management
- View incoming orders
- View customer details
- Update order statuses
- Download invoices

Supported statuses:

- Confirmed
- Packed
- Out For Delivery
- Delivered

### Business Dashboard
- Revenue metrics
- Order analytics
- Delivery statistics
- Performance overview

---

## Marketplace Administration Console

### User Management
- View platform users
- Manage user roles
- Monitor platform activity

### Boutique Management
- Boutique approval workflow
- Boutique verification
- Boutique monitoring

### Category Management
- Create categories
- Edit categories
- Delete categories

### Banner Management
- Homepage banner administration
- Marketing content control

### Order Monitoring
- View all marketplace orders
- Monitor order lifecycles
- Access invoices
- View customer and boutique information

### Marketplace Analytics
- Revenue insights
- Order statistics
- Boutique performance metrics
- Platform-wide monitoring

---

# Order Lifecycle

text Customer Places Order           │           ▼ Order Created           │           ▼ Invoice Generated           │           ▼ Boutique Receives Order           │           ▼ Order Confirmed           │           ▼ Order Packed           │           ▼ Out For Delivery           │           ▼ Delivered 

---

# Invoice System

Invoices are automatically generated immediately after a customer successfully places an order.

Generated invoices are permanently linked to their corresponding orders and remain accessible throughout the order lifecycle.

Invoices can be accessed by:

- Customers
- Boutique Partners
- Marketplace Administrators

Invoice details include:

- Invoice Number
- Order Number
- Customer Information
- Boutique Information
- Product Details
- Quantity Breakdown
- Pricing Summary
- Delivery Information
- Transaction Information

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

# Hyperlocal Delivery Engine

HIVE uses coordinate-based delivery validation to determine serviceability.

Delivery eligibility is calculated using:

- Customer coordinates
- Boutique coordinates
- Boutique delivery radius

This approach enables accurate hyperlocal delivery coverage without relying on city-level restrictions.

---

# Media Infrastructure

Cloudinary is integrated for:

- Product image storage
- Product video storage
- Boutique verification documents
- Customer claim evidence uploads
- CDN delivery
- Image transformations
- Responsive image optimization
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

## Monorepo

- Turborepo

---

# Platform Architecture

text Customer Marketplace         │         ▼      Next.js         │         ▼       Convex         │  ┌──────┼────────┬─────────┐  ▼      ▼        ▼         ▼ Clerk Cloudinary Resend Database Auth   Media     Email   Storage 

---

# Security & Access Control

### Customer

Can:

- Browse products
- Place orders
- Track orders
- Download invoices

Cannot:

- Access boutique management
- Access administration controls

### Boutique Partner

Can:

- Manage own products
- Manage own orders
- Update order statuses
- Access invoices

Cannot:

- Access administration controls
- Manage other boutiques

### Administrator

Can:

- Manage users
- Manage boutiques
- Manage categories
- Manage banners
- Monitor marketplace activity
- Access all orders

---

# Project Structure

bash apps/ ├── customer/ ├── boutique/ ├── admin/  convex/ ├── orders.ts ├── products.ts ├── boutiques.ts ├── invoices.ts ├── emails.ts ├── users.ts  packages/ ├── ui/ ├── utils/ ├── types/ 

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
- Automatic invoice generation
- Responsive mobile-first design
- Cloud-based media infrastructure
- Transactional email notification system
- Role-based access control
- Scalable monorepo architecture
- End-to-end marketplace workflow

---

## Author

Yedukrishnan K R

HIVE was developed as a full-stack hyperlocal marketplace platform demonstrating modern web architecture, real-time backend systems, role-based access control, media infrastructure, transactional workflows, and scalable marketplace operations.
