// File: App.tsx (React + Tailwind CSS)
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { MapPin, Lock, Clock } from "lucide-react";

const libraries = [
  {
    name: "City Central Library",
    price: "₹500/month",
    duration: "1 Month",
    locker: true,
    location: "Connaught Place, Delhi",
  },
  {
    name: "Green Study Library",
    price: "₹300/month",
    duration: "1 Month",
    locker: false,
    location: "Noida Sector 62",
  },
  {
    name: "BookNest Reading Hall",
    price: "₹1000/3 months",
    duration: "3 Months",
    locker: true,
    location: "Indirapuram, Ghaziabad",
  },
];

export default function App() {
  return (
    <div className="min-h-screen bg-gray-100 p-6">
      <h1 className="text-3xl font-bold text-center mb-8">📚 Local Libraries</h1>

      <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
        {libraries.map((lib, index) => (
          <Card key={index} className="rounded-2xl shadow-lg p-4">
            <CardContent>
              <h2 className="text-xl font-semibold mb-2">{lib.name}</h2>
              <p className="text-gray-700 mb-1">💰 Price: {lib.price}</p>
              <p className="flex items-center text-gray-700 mb-1">
                <Clock className="w-4 h-4 mr-2" /> Duration: {lib.duration}
              </p>
              <p className="flex items-center text-gray-700 mb-1">
                <Lock className="w-4 h-4 mr-2" />
                Locker Facility:{" "}
                <span className="font-medium ml-1">{lib.locker ? "Yes" : "No"}</span>
              </p>
              <p className="flex items-center text-gray-700">
                <MapPin className="w-4 h-4 mr-2" />
                {lib.location}
              </p>
            </CardContent>
          </Card>
        ))}
      </div>
    </div>
  );
}# Library-website-
