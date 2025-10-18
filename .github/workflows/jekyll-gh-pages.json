import React from "react";
import { Download } from "lucide-react";
import { Button } from "@/components/ui/button";

const Snowfall = () => {
  // Create an array of 150 snowflake elements
  const snowflakes = Array.from({ length: 150 }).map((_, i) => {
    const style = {
      left: `${Math.random() * 100}%`,
      width: `${Math.random() * 3 + 1}px`,
      height: `${Math.random() * 3 + 1}px`,
      animationDelay: `${Math.random() * 10}s`,
      animationDuration: `${Math.random() * 5 + 5}s`,
    };
    return <div key={i} className="snowflake" style={style} />;
  });

  return <div className="absolute top-0 left-0 w-full h-full pointer-events-none">{snowflakes}</div>;
};

export default function Home() {
  const handleDownload = () => {
    // Add your download logic here
    console.log("Download clicked");
  };

  return (
    <div className="relative min-h-screen bg-gradient-to-br from-blue-950 via-blue-900 to-black flex items-center justify-center p-6 overflow-hidden">
      <Snowfall />
      <div className="max-w-4xl mx-auto text-center z-10">
        {/* Title with animation */}
        <h1 className="text-5xl md:text-7xl lg:text-8xl font-bold text-white mb-8 animate-fade-in">
          <span className="bg-gradient-to-r from-blue-300 to-white bg-clip-text text-transparent">
            Selenite Menu
          </span>
        </h1>

        <p className="text-xl md:text-2xl text-blue-200 mb-12 max-w-2xl mx-auto">
          Experience the best mod menu. Get started by downloading now.
        </p>

        {/* Gradient Download Button */}
        <Button
          onClick={handleDownload}
          size="lg"
          className="bg-gradient-to-r from-blue-500 to-blue-700 hover:from-blue-600 hover:to-blue-800 text-white px-8 py-6 text-lg font-semibold rounded-full shadow-xl hover:shadow-2xl transform hover:scale-105 transition-all duration-300"
        >
          <Download className="w-6 h-6 mr-2" />
          Download Now
        </Button>
      </div>

      <style>{`
        .snowflake {
          position: absolute;
          top: -10px;
          background-color: white;
          border-radius: 50%;
          opacity: 0.6;
          animation-name: snowfall;
          animation-timing-function: linear;
          animation-iteration-count: infinite;
        }

        @keyframes snowfall {
          0% {
            transform: translateY(0vh) translateX(0px);
            opacity: 0.6;
          }
          100% {
            transform: translateY(105vh) translateX(20px);
            opacity: 0;
          }
        }

        @keyframes fade-in {
          from {
            opacity: 0;
            transform: translateY(-20px);
          }
          to {
            opacity: 1;
            transform: translateY(0);
          }
        }

        .animate-fade-in {
          animation: fade-in 1s ease-out;
        }
      `}</style>
    </div>
  );
}
