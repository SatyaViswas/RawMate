# RawMate

> A modern B2B marketplace platform connecting raw material suppliers with vendors through a seamless, real-time commerce experience.


[![TypeScript](https://img.shields.io/badge/TypeScript-5.5+-blue)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-18.3+-blue)](https://react.dev)
[![Vite](https://img.shields.io/badge/Vite-5.4+-blue)](https://vitejs.dev)

## Overview

RawMate is a sophisticated B2B marketplace platform designed to streamline the sourcing and distribution of raw materials. The platform facilitates real-time transactions between suppliers (sellers) and vendors (buyers), offering a comprehensive suite of features including product management, order processing, real-time inventory tracking, and supplier reviews.

## ✨ Key Features

### For Vendors (Buyers)
- **Product Discovery**: Browse and search a comprehensive catalog of raw materials from multiple suppliers
- **Supplier Comparison**: Compare offerings, pricing, and ratings across different suppliers
- **Shopping Cart**: Add products to cart with real-time quantity management and synchronization
- **Order Management**: Track incoming and historical orders with status updates and detailed information
- **Supplier Reviews**: Leave ratings and reviews based on product quality, delivery time, and service
- **Account Management**: Maintain business profile, contact information, and preferences
- **Real-time Notifications**: Stay updated on order status changes and supplier communications

### For Suppliers (Sellers)
- **Product Management**: Create, edit, and manage product listings with pricing and availability
- **Order Processing**: Receive and process incoming orders from vendors with order details
- **Inventory Management**: Track product stock and availability in real-time
- **Performance Analytics**: View supplier ratings and customer reviews to improve service quality
- **Account Management**: Manage business profile, contact information, and bank details
- **Business Insights**: Monitor sales performance and vendor interactions

### Platform Features
- **Dual Role Authentication**: Secure login system for both vendors and suppliers with email verification
- **Role-Based Access Control**: Separate dashboards and features tailored to each user role
- **Real-Time Data Synchronization**: Account updates propagate instantly across the platform
- **Responsive Design**: Fully responsive UI optimized for desktop and mobile devices
- **Dark Mode Support**: Built-in theme switching for comfortable viewing
- **Form Validation**: Comprehensive validation with real-time user feedback
- **Error Handling**: Graceful error handling with informative user messages

## 🏗️ Architecture

### Technology Stack

#### Frontend
- **Framework**: [React 18.3](https://react.dev) - Modern UI library with hooks and concurrent rendering
- **Build Tool**: [Vite 5.4](https://vitejs.dev) - Lightning-fast build tool and dev server
- **Language**: [TypeScript 5.5](https://www.typescriptlang.org/) - Type-safe JavaScript
- **Routing**: [React Router 6.26](https://reactrouter.com/) - Client-side routing and navigation
- **Form Management**: [React Hook Form 7.53](https://react-hook-form.com/) - Performant form validation
- **State Management**: [TanStack Query 5.56](https://tanstack.com/query/latest) - Server state management and caching
- **UI Components**: [shadcn/ui](https://ui.shadcn.com/) - High-quality, accessible React components
- **Styling**: [Tailwind CSS 3.4](https://tailwindcss.com/) - Utility-first CSS framework
- **Icons**: [Lucide React 0.462](https://lucide.dev/) - Beautiful, consistent icon library
- **Charts**: [Recharts 2.12](https://recharts.org/) - Composable charting library

#### Backend
- **Database**: [Supabase](https://supabase.com/) - PostgreSQL-based BaaS platform
- **Authentication**: Supabase Auth with email-based signup and verification
- **Real-time Features**: Supabase Realtime for instant data synchronization
- **Row-Level Security (RLS)**: PostgreSQL policies for data access control

#### UI Components & Utilities
- **Form Validation**: [Zod 3.23](https://zod.dev/) - TypeScript-first schema validation
- **Accessibility**: [Radix UI](https://www.radix-ui.com/) - Primitive components with accessibility built-in
- **Animations**: [Tailwind CSS Animate](https://github.com/jamiebuilds/tailwindcss-animate)
- **Notifications**: [Sonner 1.5](https://sonner.emilkowal.ski/) - Toast notifications
- **Command Palette**: [cmdk 1.0](https://cmdk.paco.me/) - Fast command menu

### Project Structure

```
RawMate/
├── src/
│   ├── pages/                      # Page components
│   │   ├── vendor/                # Vendor (buyer) pages
│   │   │   ├── VendorDashboard.tsx
│   │   │   ├── BrowseProducts.tsx
│   │   │   ├── Cart.tsx
│   │   │   ├── MyOrders.tsx
│   │   │   ├── CompareSuppliers.tsx
│   │   │   ├── VendorReviews.tsx
│   │   │   └── AccountSettings.tsx
│   │   ├── supplier/              # Supplier (seller) pages
│   │   │   ├── SupplierDashboard.tsx
│   │   │   ├── MyProducts.tsx
│   │   │   ├── AddProduct.tsx
│   │   │   ├── EditProduct.tsx
│   │   │   ├── IncomingOrders.tsx
│   │   │   ├── SupplierReviews.tsx
│   │   │   └── AccountSettings.tsx
│   │   ├── Welcome.tsx            # Landing page
│   │   ├── VendorLogin.tsx        # Vendor login
│   │   ├── SupplierLogin.tsx      # Supplier login
│   │   └── Index.tsx              # Main entry point
│   ├── components/
│   │   ├── layouts/               # Layout components
│   │   ├── ui/                    # shadcn/ui components
│   │   ├── AuthForm.tsx           # Authentication form
│   │   ├── VendorLayout.tsx       # Vendor layout wrapper
│   │   ├── SupplierLayout.tsx     # Supplier layout wrapper
│   │   ├── VendorSidebar.tsx      # Navigation sidebar
│   │   └── SupplierSidebar.tsx    # Navigation sidebar
│   ├── contexts/                  # React Context API contexts
│   │   └── CartContext.tsx        # Shopping cart state
│   ├── hooks/                     # Custom React hooks
│   │   ├── useAuth.ts             # Authentication logic
│   │   ├── useProducts.ts         # Product data fetching
│   │   ├── useOrders.ts           # Order data fetching
│   │   └── useSuppliers.ts        # Supplier data fetching
│   ├── lib/                       # Utility functions
│   ├── integrations/              # Third-party integrations
│   ├── assets/                    # Images, fonts, etc.
│   ├── App.tsx                    # Main app component
│   ├── main.tsx                   # Entry point
│   └── index.css                  # Global styles
├── supabase/
│   ├── config.toml               # Supabase configuration
│   └── migrations/               # Database migrations
├── public/                        # Static assets
├── vite.config.ts                # Vite configuration
├── tailwind.config.ts            # Tailwind CSS configuration
├── tsconfig.json                 # TypeScript configuration
├── package.json                  # Dependencies and scripts
└── eslint.config.js              # ESLint configuration
```

## 🚀 Getting Started

### Prerequisites

- **Node.js**: v18.0.0 or higher
- **Bun**: v1.0.0 or higher (or npm/yarn as alternatives)
- **Git**: Latest version

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd RawMate
   ```

2. **Install dependencies**
   ```bash
   bun install
   # or
   npm install
   # or
   yarn install
   ```

3. **Configure environment variables**

   Create a `.env.local` file in the project root with your Supabase credentials:
   ```env
   VITE_SUPABASE_URL=your_supabase_project_url
   VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

   Get these values from your [Supabase project settings](https://supabase.com/dashboard).

4. **Start the development server**
   ```bash
   bun run dev
   # or
   npm run dev
   ```

   The application will be available at `http://localhost:8080`

## 📦 Build & Deployment

### Development Build
```bash
bun run build:dev
# or
npm run build:dev
```

### Production Build
```bash
bun run build
# or
npm run build
```

### Preview Production Build
```bash
bun run preview
# or
npm run preview
```

### Code Quality

#### Linting
```bash
bun run lint
# or
npm run lint
```

## 🔐 Authentication & Security

### User Roles

**Vendor (Buyer)**
- Browse and purchase raw materials
- Manage orders and payments
- Leave supplier reviews
- Compare supplier offerings

**Supplier (Seller)**
- List and manage products
- Process incoming orders
- Receive customer reviews
- Track sales performance

### Authentication Flow

1. User selects role (Vendor or Supplier) on login page
2. Email-based authentication with Supabase Auth
3. Email verification for new accounts
4. JWT token-based session management
5. Automatic role-based routing to appropriate dashboard

### Security Features

- **Row-Level Security (RLS)**: PostgreSQL policies ensure users can only access their own data
- **Email Verification**: Prevents unauthorized account creation
- **Type Safety**: TypeScript prevents common security vulnerabilities
- **Secure Token Storage**: JWT tokens managed securely by Supabase
- **Input Validation**: Zod schema validation on all forms

## 🗄️ Database Schema

The application uses PostgreSQL via Supabase with the following main entities:

- **Users**: Authentication and profile information (vendors and suppliers)
- **Products**: Product listings managed by suppliers
- **Orders**: Purchase orders from vendors to suppliers
- **Cart Items**: Shopping cart management for vendors
- **Reviews**: Supplier reviews and ratings from vendors

Database migrations are stored in `supabase/migrations/` and can be applied via the Supabase dashboard or CLI.

## 🎨 UI/UX Design

### Design System

- **Component Library**: shadcn/ui with Radix UI primitives
- **Styling**: Tailwind CSS utility classes
- **Responsiveness**: Mobile-first design approach
- **Accessibility**: WCAG 2.1 AA compliance with semantic HTML

### Theme Support

- Light mode (default)
- Dark mode support via `next-themes`
- Configurable in `tailwind.config.ts`

## 📝 Development Guidelines

### Code Style

- **TypeScript**: Strict mode enabled for type safety
- **ESLint**: Configured for React and TypeScript best practices
- **Formatting**: Use IDE formatting on save

### Component Development

```typescript
import React from 'react';
import { Button } from '@/components/ui/button';

interface MyComponentProps {
  title: string;
  onClick?: () => void;
}

export const MyComponent: React.FC<MyComponentProps> = ({ 
  title, 
  onClick 
}) => {
  return (
    <div>
      <h1>{title}</h1>
      <Button onClick={onClick}>Click me</Button>
    </div>
  );
};
```

### Form Development

Using React Hook Form with Zod validation:

```typescript
import { useForm } from 'react-hook-form';
import { zodResolver } from '@hookform/resolvers/zod';
import { z } from 'zod';

const schema = z.object({
  email: z.string().email(),
  password: z.string().min(8),
});

export const MyForm = () => {
  const { register, handleSubmit, formState: { errors } } = useForm({
    resolver: zodResolver(schema),
  });

  return (
    <form onSubmit={handleSubmit((data) => console.log(data))}>
      <input {...register('email')} />
      {errors.email && <span>{errors.email.message}</span>}
    </form>
  );
};
```

### Data Fetching

Using TanStack Query (React Query):

```typescript
import { useQuery } from '@tanstack/react-query';

export const useProducts = () => {
  return useQuery({
    queryKey: ['products'],
    queryFn: async () => {
      const { data, error } = await supabase
        .from('products')
        .select('*');
      if (error) throw error;
      return data;
    },
  });
};
```

## 🧪 Testing

Currently, the project uses manual testing. Consider adding:

- **Unit Tests**: Jest with React Testing Library
- **E2E Tests**: Playwright or Cypress for user flows
- **Integration Tests**: API testing with Supabase

## 🐛 Troubleshooting

### Development Server Issues

**Issue**: Port 8080 is already in use
```bash
# Kill the process using port 8080
lsof -ti:8080 | xargs kill -9
```

### Authentication Issues

**Issue**: Users can't log in
- Verify Supabase credentials in `.env.local`
- Check that email verification is enabled in Supabase settings
- Ensure database migrations have been applied

### Data Not Appearing

**Issue**: Products or orders not showing
- Verify Row-Level Security policies in Supabase
- Check browser console for errors
- Ensure user is properly authenticated
- Verify data exists in the Supabase dashboard

### Build Errors

**Issue**: TypeScript compilation errors
```bash
# Clear cache and reinstall
rm -rf node_modules
bun install
bun run build
```

## 📚 Resources

### Documentation
- [React Documentation](https://react.dev)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [Vite Guide](https://vitejs.dev/guide/)
- [Supabase Documentation](https://supabase.com/docs)
- [React Router Documentation](https://reactrouter.com/)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

### Component Libraries
- [shadcn/ui Components](https://ui.shadcn.com/docs)
- [Radix UI Primitives](https://www.radix-ui.com/docs/primitives)
- [Lucide Icons](https://lucide.dev/)

### Tools & Libraries
- [React Hook Form Docs](https://react-hook-form.com/get-started)
- [TanStack Query Documentation](https://tanstack.com/query/latest)
- [Zod Schema Validation](https://zod.dev/)

## 🤝 Contributing

We welcome contributions to RawMate! Please follow these guidelines:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Commit Message Guidelines

- Use clear, descriptive commit messages
- Prefix with type: `feat:`, `fix:`, `docs:`, `style:`, `refactor:`, `test:`
- Example: `feat: add product search functionality`


---

<div align="center">

**[↑ Back to Top](#rawmate)**

Made with ❤️ by the RawMate team

</div>

