import React from 'react';
import { 
  Camera, Code, Database, Cloud, Server, 
  Linkedin, Mail, Globe, GitBranch, 
  Gamepad, HardDrive 
} from 'lucide-react';

const GithubProfile = () => {
  const technologies = {
    languages: [
      { name: 'JavaScript', logo: 'javascript', color: 'bg-yellow-500' },
      { name: 'TypeScript', logo: 'typescript', color: 'bg-blue-600' },
      { name: 'Python', logo: 'python', color: 'bg-blue-400' },
      { name: 'GoLang', logo: 'go', color: 'bg-cyan-500' },
      { name: 'Solidity', logo: 'solidity', color: 'bg-gray-700' }
    ],
    backends: [
      { name: 'Node.js', logo: 'nodejs', color: 'bg-green-600' },
      { name: 'NestJS', logo: 'nestjs', color: 'bg-red-500' },
      { name: 'ExpressJS', logo: 'express', color: 'bg-gray-900' }
    ],
    databases: [
      { name: 'PostgreSQL', logo: 'postgresql', color: 'bg-blue-800' },
      { name: 'MongoDB', logo: 'mongodb', color: 'bg-green-500' },
      { name: 'Redis', logo: 'redis', color: 'bg-red-600' }
    ]
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-gray-100 to-gray-200 p-8 font-sans">
      <div className="max-w-4xl mx-auto bg-white shadow-2xl rounded-2xl overflow-hidden">
        <div className="relative">
          <div className="absolute top-6 right-6 flex space-x-3">
            <a href="https://linkedin.com/in/mohamed-tarek-fouad" 
               className="text-blue-600 hover:text-blue-800 transition-colors">
              <Linkedin size={28} />
            </a>
            <a href="mailto:mohamed.tarek.fouad619@gmail.com" 
               className="text-red-600 hover:text-red-800 transition-colors">
              <Mail size={28} />
            </a>
          </div>
          
          <div className="p-8 text-center">
            <img 
              src="/api/placeholder/300/300" 
              alt="Mohamed Tarek" 
              className="w-48 h-48 rounded-full mx-auto border-4 border-white shadow-lg object-cover"
            />
            <h1 className="text-4xl font-bold text-gray-800 mt-4">
              Mohamed Tarek
            </h1>
            <p className="text-xl text-gray-600 mt-2">
              Backend Developer | System Architect
            </p>
          </div>
        </div>
        
        <div className="grid md:grid-cols-3 gap-6 p-8 bg-gray-50">
          {Object.entries(technologies).map(([category, items]) => (
            <div key={category} className="bg-white rounded-xl shadow-md p-6">
              <h2 className="text-2xl font-semibold mb-4 text-gray-700 capitalize">
                {category}
              </h2>
              <div className="space-y-3">
                {items.map(tech => (
                  <div 
                    key={tech.name} 
                    className="flex items-center space-x-3 bg-gray-100 p-3 rounded-lg hover:bg-gray-200 transition-colors"
                  >
                    <div className={`w-10 h-10 ${tech.color} rounded-full flex items-center justify-center`}>
                      <Code className="text-white" size={20} />
                    </div>
                    <span className="text-gray-800 font-medium">{tech.name}</span>
                  </div>
                ))}
              </div>
            </div>
          ))}
        </div>
        
        <div className="bg-gradient-to-r from-blue-500 to-purple-600 text-white p-8 text-center">
          <h2 className="text-3xl font-bold mb-4">Fun Facts</h2>
          <div className="flex justify-center space-x-8">
            <div className="flex items-center space-x-3">
              <HardDrive className="text-yellow-300" />
              <span>Blockchain Enthusiast</span>
            </div>
            <div className="flex items-center space-x-3">
              <Gamepad className="text-green-300" />
              <span>Strategy Game Player</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  );
};

export default GithubProfile;
