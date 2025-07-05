# Olympics Database Management System

A comprehensive database management system for Olympic Games data, built with MySQL and Python. This project manages various aspects of Olympic events including athletes, sports, venues, awards, audience, and business operations.

## 🏅 Project Overview

The Olympics Database Management System provides a complete solution for managing Olympic Games data with the following key features:

- **Athlete Management**: Track sportspeople, coaches, and their performance records
- **Event Organization**: Manage sports, venues, equipment, and scheduling
- **Award Tracking**: Record medals and achievements by athletes and countries
- **Audience & Business**: Handle ticket sales, purchases, and business partnerships
- **Operational Management**: Organize teams for logistics, security, and event coordination

## 🗃️ Database Schema

### Core Entities

- **SPORTSPEOPLE**: Athletes and coaches with personal details and statistics
- **SPORTS**: Various Olympic sports with rules, divisions, and participation details
- **PLAYING_ARENA**: Venues with location coordinates and condition status
- **AWARDS**: Medal records linked to sports and years
- **AUDIENCE**: Ticket holders and spectators information
- **BUSINESSES**: Corporate sponsors and vendors
- **EMPLOYEES**: Staff management with hierarchical structure
- **INVENTORY**: Sports equipment and facility resources

### Specialized Tables

- **MANAGEMENT**: Organizational teams (Logistics, Security, Finance, etc.)
- **ATHLETES**: Athlete-specific records and achievements
- **COACHES**: Coaching staff with experience details
- **TRAINING**: Coach-athlete relationships

## 🚀 Features

### Query Operations
1. **Age-based Athlete Search** - Find sportspeople older than specified age
2. **Country-wise Athlete Listing** - Get athletes from specific countries
3. **Medal Count Analysis** - Total medals won by countries
4. **Equipment Search** - Find inventory items containing specific terms
5. **Advanced Filtering** - Multi-criteria athlete searches
6. **Award Analysis** - Detailed award information by various filters
7. **Purchase Analytics** - Business transaction analysis
8. **Data Management** - Insert, update, and delete operations

### Management Features
- Hierarchical employee structure with supervisor relationships
- Team-based organization for different operational aspects
- Equipment tracking with status monitoring
- Venue management with geographic coordinates
- Financial tracking for businesses and budgets