import React from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { motion } from "framer-motion";

export default function MealmetricWebsite() { return ( <div className="p-6 grid gap-10"> {/* Header */} <motion.h1 initial={{ opacity: 0, y: -20 }} animate={{ opacity: 1, y: 0 }} className="text-4xl font-bold text-center" > Mealmetric Private Limited </motion.h1>

<p className="text-center text-lg">
    Ghar jaisa healthy tiffin – Trusted local providers se direct order karein
  </p>

  {/* Auth Section */}
  <div className="flex justify-center gap-4">
    <Button className="rounded-2xl">Customer Login</Button>
    <Button className="rounded-2xl">Vendor Signup</Button>
  </div>

  {/* Services */}
  <div className="grid md:grid-cols-4 gap-4">
    {[
      "Daily Tiffin Service",
      "Weekly Subscription",
      "Monthly Plans",
      "Affordable Home Food",
    ].map((item) => (
      <Card key={item} className="rounded-2xl shadow">
        <CardContent className="p-4 text-center font-medium">
          {item}
        </CardContent>
      </Card>
    ))}
  </div>

  {/* Order Process */}
  <div className="grid md:grid-cols-4 gap-4">
    {[
      "Signup/Login",
      "Choose Tiffin",
      "Online Payment",
      "Track Order",
    ].map((step) => (
      <Card key={step} className="rounded-2xl shadow">
        <CardContent className="p-4 text-center">
          {step}
        </CardContent>
      </Card>
    ))}
  </div>

  {/* CTA */}
  <div className="text-center">
    <Button className="rounded-2xl text-lg px-6">Order Tiffin Now</Button>
  </div>

  {/* Contact */}
  <div className="text-center text-sm opacity-70">
    Contact: info@mealmetric.com
  </div>
</div>

); }
