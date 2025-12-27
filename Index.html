import React, { useState, useEffect } from 'react';
import { Heart, Users, TrendingUp, Menu, X, Home, HandHeart, BookOpen, DollarSign, Eye, EyeOff, LogOut, ChevronLeft, ChevronRight, CheckCircle, ArrowRight } from 'lucide-react';

const CONFIG = {
  platformName: 'Kebaikan Kita',
  bankName: 'Bank Central Asia (BCA)',
  accountNumber: '00000000',
  accountHolder: 'FIRMAN SUTARMAN HASAN',
  whatsapp: '08000000000',
  email: 'Hasan@gmail.com',
  instagram: '@KebaikanKita',
  adminPassword: 'Hasan0526',
  platformFee: 0.10,
  primaryColor: '#9CAF2F',
  primaryDark: '#7A8C24'
};

const INITIAL_CAMPAIGNS = [
  { id: '1', title: 'Bantu Biaya Operasi Ibu Siti', category: 'infaq', target: 25000000, collected: 18500000, donors: 87, story: 'Ibu Siti membutuhkan operasi segera.', status: 'active', urgent: true },
  { id: '2', title: 'Wakaf Masjid Al-Ikhlas', category: 'wakaf', target: 500000000, collected: 234000000, donors: 456, story: 'Pembangunan masjid untuk umat.', status: 'active', urgent: true },
  { id: '3', title: 'Qurban Sapi Dhuafa', category: 'qurban', target: 20000000, collected: 12500000, donors: 34, story: 'Qurban untuk keluarga dhuafa.', status: 'active', urgent: false },
  { id: '4', title: 'Zakat Fitrah 1446 H', category: 'zakat', target: 50000000, collected: 35000000, donors: 234, story: 'Penyaluran zakat fitrah.', status: 'active', urgent: true },
  { id: '5', title: 'Pendidikan Anak Yatim', category: 'infaq', target: 150000000, collected: 89000000, donors: 234, story: 'Program pendidikan anak yatim.', status: 'active', urgent: false },
  { id: '6', title: 'Bantuan Korban Bencana', category: 'infaq', target: 100000000, collected: 45000000, donors: 156, story: 'Bantuan darurat bencana.', status: 'active', urgent: false }
];

const INITIAL_DONATIONS = [
  { id: '1', campaignId: '1', name: 'Ahmad', amount: 500000, status: 'verified', createdAt: new Date().toISOString() },
  { id: '2', campaignId: '1', name: 'Hamba Allah', amount: 100000, status: 'verified', createdAt: new Date().toISOString() },
  { id: '3', campaignId: '2', name: 'Fatimah', amount: 1000000, status: 'pending', createdAt: new Date().toISOString() }
];

export default function App() {
  const [view, setView] = useState('home');
  const [selectedCategory, setSelectedCategory] = useState(null);
  const [selectedCampaign, setSelectedCampaign] = useState(null);
  const [isAdmin, setIsAdmin] = useState(false);
  const [campaigns, setCampaigns] = useState(INITIAL_CAMPAIGNS);
  const [donations, setDonations] = useState(INITIAL_DONATIONS);
  const [showMenu, setShowMenu] = useState(false);

  useEffect(() => {
    if (window.location.hash === '#admin') setView('admin-login');
  }, []);

  const navigate = (v, cat = null, camp = null) => {
    setView(v);
    setSelectedCategory(cat);
    setSelectedCampaign(camp);
    setShowMenu(false);
  };

  return (
    <div className="min-h-screen bg-gray-50">
      <Navbar navigate={navigate} isAdmin={isAdmin} setIsAdmin={setIsAdmin} showMenu={showMenu} setShowMenu={setShowMenu} />
      
      {view === 'home' && !selectedCategory && <HomePage navigate={navigate} campaigns={campaigns} />}
      {view === 'home' && selectedCategory && <CategoryPage category={selectedCategory} campaigns={campaigns.filter(c => c.category === selectedCategory)} navigate={navigate} />}
      {view === 'campaign' && <CampaignPage campaign={selectedCampaign} donations={donations.filter(d => d.campaignId === selectedCampaign?.id)} navigate={navigate} />}
      {view === 'donation' && <DonationPage campaign={selectedCampaign} navigate={navigate} setDonations={setDonations} />}
      {view === 'admin-login' && <AdminLogin navigate={navigate} setIsAdmin={setIsAdmin} />}
      {view === 'admin' && isAdmin && <AdminPanel campaigns={campaigns} setCampaigns={setCampaigns} donations={donations} setDonations={setDonations} navigate={navigate} setIsAdmin={setIsAdmin} />}
      {view === 'calculator' && <Calculator navigate={navigate} />}
      {view === 'about' && <About navigate={navigate} />}
      
      <Footer />
    </div>
  );
}

function Navbar({ navigate, isAdmin, setIsAdmin, showMenu, setShowMenu }) {
  const showAdminBtn = isAdmin || window.location.hash === '#admin';
  
  return (
    <nav className="bg-white shadow sticky top-0 z-50">
      <div className="max-w-7xl mx-auto px-4">
        <div className="flex justify-between items-center h-16">
          <button onClick={() => navigate('home')} className="flex items-center gap-2">
            <div className="w-10 h-10 rounded-full flex items-center justify-center" style={{ backgroundColor: CONFIG.primaryColor }}>
              <Heart className="text-white" size={20} fill="white" />
            </div>
            <span className="font-bold text-lg">{CONFIG.platformName}</span>
          </button>

          <div className="hidden md:flex gap-6 items-center">
            <button onClick={() => navigate('home')}>Beranda</button>
            <button onClick={() => navigate('about')}>Tentang</button>
            <button onClick={() => navigate('calculator')}>Kalkulator</button>
            {showAdminBtn && (
              isAdmin ? (
                <>
                  <button onClick={() => navigate('admin')} className="px-4 py-2 text-white rounded" style={{ backgroundColor: CONFIG.primaryColor }}>Dashboard</button>
                  <button onClick={() => { setIsAdmin(false); navigate('home'); }}><LogOut size={20} /></button>
                </>
              ) : (
                <button onClick={() => navigate('admin-login')} className="px-4 py-2 text-white rounded" style={{ backgroundColor: CONFIG.primaryColor }}>Admin</button>
              )
            )}
          </div>

          <button onClick={() => setShowMenu(!showMenu)} className="md:hidden">
            {showMenu ? <X size={24} /> : <Menu size={24} />}
          </button>
        </div>

        {showMenu && (
          <div className="md:hidden pb-4 space-y-2">
            <button onClick={() => navigate('home')} className="block w-full text-left px-4 py-2">Beranda</button>
            <button onClick={() => navigate('about')} className="block w-full text-left px-4 py-2">Tentang</button>
            <button onClick={() => navigate('calculator')} className="block w-full text-left px-4 py-2">Kalkulator</button>
          </div>
        )}
      </div>
    </nav>
  );
}

function HomePage({ navigate, campaigns }) {
  const categories = [
    { id: 'zakat', name: 'Zakat', icon: BookOpen },
    { id: 'wakaf', name: 'Wakaf', icon: Home },
    { id: 'infaq', name: 'Infaq', icon: HandHeart },
    { id: 'qurban', name: 'Qurban', icon: DollarSign }
  ];

  return (
    <>
      <section className="max-w-7xl mx-auto px-4 pt-8">
        <div className="rounded-2xl p-12 text-white" style={{ background: `linear-gradient(135deg, ${CONFIG.primaryColor}, ${CONFIG.primaryDark})` }}>
          <p className="mb-2">بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيم</p>
          <h1 className="text-4xl font-bold mb-4">Berbagi Kebaikan, Raih Berkah</h1>
          <p className="text-lg">Platform donasi Islami terpercaya</p>
        </div>
      </section>

      <section className="max-w-7xl mx-auto px-4 py-8">
        <div className="grid grid-cols-2 md:grid-cols-4 gap-4">
          {categories.map(cat => {
            const Icon = cat.icon;
            return (
              <button
                key={cat.id}
                onClick={() => navigate('home', cat.id)}
                className="flex flex-col items-center gap-3 p-6 bg-white rounded-2xl hover:shadow-lg transition"
              >
                <div className="w-16 h-16 rounded-full flex items-center justify-center" style={{ backgroundColor: `${CONFIG.primaryColor}20` }}>
                  <Icon size={32} style={{ color: CONFIG.primaryColor }} />
                </div>
                <span className="font-semibold">{cat.name}</span>
              </button>
            );
          })}
        </div>
      </section>

      <section className="max-w-7xl mx-auto px-4 py-8">
        <h2 className="text-2xl font-bold mb-6">Program Prioritas</h2>
        <div className="grid md:grid-cols-3 gap-6">
          {campaigns.slice(0, 6).map(c => (
            <CampaignCard key={c.id} campaign={c} onClick={() => navigate('campaign', null, c)} />
          ))}
        </div>
      </section>
    </>
  );
}

function CategoryPage({ category, campaigns, navigate }) {
  const [visible, setVisible] = useState(6);
  const [slide, setSlide] = useState(0);
  
  const urgent = campaigns.filter(c => c.urgent);
  const hasMore = visible < campaigns.length;

  return (
    <div className="max-w-7xl mx-auto px-4 py-8">
      <button onClick={() => navigate('home')} className="mb-6" style={{ color: CONFIG.primaryColor }}>← Kembali</button>
      
      <h1 className="text-3xl font-bold mb-8 capitalize">{category}</h1>

      {urgent.length > 0 && (
        <div className="mb-12 relative bg-white rounded-2xl shadow-lg overflow-hidden">
          <div className="md:flex">
            <div className="md:w-1/3 bg-gray-200 h-64 flex items-center justify-center">
              <p className="text-gray-500">[Foto]</p>
            </div>
            <div className="md:w-2/3 p-8">
              <span className="px-3 py-1 rounded-full text-xs font-semibold mb-3 inline-block" style={{ backgroundColor: `${CONFIG.primaryColor}20`, color: CONFIG.primaryColor }}>MENDESAK</span>
              <h3 className="text-2xl font-bold mb-3">{urgent[slide]?.title}</h3>
              <p className="text-gray-600 mb-4">{urgent[slide]?.story}</p>
              <button onClick={() => navigate('campaign', null, urgent[slide])} className="px-6 py-3 text-white rounded-lg font-semibold" style={{ backgroundColor: CONFIG.primaryColor }}>
                Donasi Sekarang
              </button>
            </div>
          </div>
          {urgent.length > 1 && (
            <>
              <button onClick={() => setSlide((slide - 1 + urgent.length) % urgent.length)} className="absolute left-4 top-1/2 -translate-y-1/2 w-10 h-10 bg-white rounded-full shadow flex items-center justify-center">
                <ChevronLeft />
              </button>
              <button onClick={() => setSlide((slide + 1) % urgent.length)} className="absolute right-4 top-1/2 -translate-y-1/2 w-10 h-10 bg-white rounded-full shadow flex items-center justify-center">
                <ChevronRight />
              </button>
            </>
          )}
        </div>
      )}

      <div className="grid md:grid-cols-3 gap-6 mb-8">
        {campaigns.slice(0, visible).map(c => (
          <CampaignCard key={c.id} campaign={c} onClick={() => navigate('campaign', null, c)} />
        ))}
      </div>

      {hasMore && (
        <div className="text-center">
          <button onClick={() => setVisible(v => v + 6)} className="px-8 py-3 border-2 rounded-lg font-semibold" style={{ borderColor: CONFIG.primaryColor, color: CONFIG.primaryColor }}>
            Load more
          </button>
        </div>
      )}
    </div>
  );
}

function CampaignPage({ campaign, donations, navigate }) {
  const pct = (campaign.collected / campaign.target) * 100;
  
  return (
    <div className="max-w-4xl mx-auto px-4 py-12">
      <button onClick={() => navigate('home', campaign.category)} className="mb-6" style={{ color: CONFIG.primaryColor }}>← Kembali</button>
      
      <div className="bg-gray-200 rounded-xl h-96 mb-8 flex items-center justify-center">
        <p className="text-gray-500">[Foto Campaign]</p>
      </div>

      <div className="bg-white rounded-xl shadow-lg p-8 mb-8">
        <h1 className="text-3xl font-bold mb-4">{campaign.title}</h1>
        
        <div className="mb-6">
          <div className="flex justify-between mb-2">
            <span className="font-semibold" style={{ color: CONFIG.primaryColor }}>Rp {campaign.collected.toLocaleString()}</span>
            <span className="text-gray-600">dari Rp {campaign.target.toLocaleString()}</span>
          </div>
          <div className="w-full bg-gray-200 rounded-full h-3">
            <div className="h-3 rounded-full" style={{ width: `${Math.min(pct, 100)}%`, background: `linear-gradient(90deg, ${CONFIG.primaryColor}, ${CONFIG.primaryDark})` }}></div>
          </div>
          <p className="mt-2 text-sm">{pct.toFixed(0)}% • {campaign.donors} donatur</p>
        </div>

        <button onClick={() => navigate('donation', null, campaign)} className="w-full text-white py-4 rounded-lg font-semibold mb-6" style={{ background: `linear-gradient(135deg, ${CONFIG.primaryColor}, ${CONFIG.primaryDark})` }}>
          Donasi Sekarang
        </button>

        <div>
          <h2 className="text-xl font-bold mb-4">Cerita</h2>
          <p className="text-gray-700">{campaign.story}</p>
        </div>
      </div>

      <div className="bg-white rounded-xl shadow-lg p-8">
        <h2 className="text-xl font-bold mb-6">Donasi Terbaru</h2>
        {donations.slice(0, 5).map(d => (
          <div key={d.id} className="flex justify-between py-3 border-b">
            <div>
              <p className="font-semibold">{d.name}</p>
              <p className="text-sm text-gray-600">{new Date(d.createdAt).toLocaleString('id-ID')}</p>
            </div>
            <p className="font-bold" style={{ color: CONFIG.primaryColor }}>Rp {d.amount.toLocaleString()}</p>
          </div>
        ))}
      </div>
    </div>
  );
}

function DonationPage({ campaign, navigate, setDonations }) {
  const [form, setForm] = useState({ name: '', email: '', whatsapp: '', amount: '', coverFee: false, anonymous: false });
  const [done, setDone] = useState(false);
  const [id, setId] = useState('');

  const fee = form.amount ? parseInt(form.amount) * CONFIG.platformFee : 0;
  const total = form.amount ? parseInt(form.amount) + (form.coverFee ? fee : 0) : 0;
  const unique = total ? total + Math.floor(Math.random() * 900) + 100 : 0;

  const handleSubmit = (e) => {
    e.preventDefault();
    const newId = `DON-${Date.now()}`;
    setDonations(prev => [...prev, {
      id: newId,
      campaignId: campaign.id,
      name: form.anonymous ? 'Hamba Allah' : form.name,
      email: form.email,
      amount: parseInt(form.amount),
      status: 'pending',
      createdAt: new Date().toISOString()
    }]);
    setId(newId);
    setDone(true);
  };

  if (done) {
    return (
      <div className="max-w-2xl mx-auto px-4 py-12">
        <div className="bg-white rounded-xl shadow-lg p-8 text-center">
          <CheckCircle size={64} className="mx-auto mb-4" style={{ color: CONFIG.primaryColor }} />
          <h1 className="text-2xl font-bold mb-2">Barakallahu Fiik!</h1>
          <p className="mb-6">ID: {id}</p>
          
          <div className="p-6 rounded-lg mb-6 border-2" style={{ backgroundColor: `${CONFIG.primaryColor}10`, borderColor: CONFIG.primaryColor }}>
            <p className="font-semibold mb-2">Transfer ke:</p>
            <p className="text-lg">{CONFIG.bankName}</p>
            <p className="text-2xl font-bold" style={{ color: CONFIG.primaryColor }}>{CONFIG.accountNumber}</p>
            <p className="mb-4">a.n. {CONFIG.accountHolder}</p>
            <p className="font-semibold mb-2">Nominal:</p>
            <p className="text-3xl font-bold" style={{ color: CONFIG.primaryColor }}>Rp {unique.toLocaleString()}</p>
          </div>

          <button onClick={() => navigate('home')} className="w-full border py-3 rounded-lg font-semibold">Kembali</button>
        </div>
      </div>
    );
  }

  return (
    <div className="max-w-2xl mx-auto px-4 py-12">
      <div className="bg-white rounded-xl shadow-lg p-8">
        <h1 className="text-2xl font-bold mb-6">Form Donasi</h1>
        <form onSubmit={handleSubmit} className="space-y-4">
          <div>
            <label className="block font-semibold mb-2">Nama</label>
            <input required value={form.name} onChange={e => setForm({ ...form, name: e.target.value })} className="w-full border rounded px-4 py-3" />
          </div>
          <div>
            <label className="block font-semibold mb-2">Email</label>
            <input type="email" required value={form.email} onChange={e => setForm({ ...form, email: e.target.value })} className="w-full border rounded px-4 py-3" />
          </div>
          <div>
            <label className="block font-semibold mb-2">WhatsApp</label>
            <input required value={form.whatsapp} onChange={e => setForm({ ...form, whatsapp: e.target.value })} className="w-full border rounded px-4 py-3" />
          </div>
          <div>
            <label className="block font-semibold mb-2">Nominal</label>
            <input type="number" required value={form.amount} onChange={e => setForm({ ...form, amount: e.target.value })} className="w-full border rounded px-4 py-3" min="10000" />
          </div>
          {form.amount && (
            <div className="bg-gray-50 p-4 rounded">
              <div className="flex justify-between mb-2"><span>Donasi</span><span>Rp {parseInt(form.amount).toLocaleString()}</span></div>
              <div className="flex justify-between mb-2"><span>Fee (10%)</span><span>{form.coverFee ? `Rp ${fee.toLocaleString()}` : 'Potong'}</span></div>
              <div className="flex justify-between font-bold border-t pt-2"><span>Total</span><span style={{ color: CONFIG.primaryColor }}>Rp {total.toLocaleString()}</span></div>
            </div>
          )}
          <button type="submit" className="w-full text-white py-4 rounded-lg font-semibold" style={{ background: `linear-gradient(135deg, ${CONFIG.primaryColor}, ${CONFIG.primaryDark})` }}>
            Lanjut
          </button>
        </form>
      </div>
    </div>
  );
}

function AdminLogin({ navigate, setIsAdmin }) {
  const [pw, setPw] = useState('');
  const [err, setErr] = useState('');

  const handleLogin = (e) => {
    e.preventDefault();
    if (pw === CONFIG.adminPassword) {
      setIsAdmin(true);
      navigate('admin');
    } else {
      setErr('Password salah!');
    }
  };

  return (
    <div className="min-h-screen flex items-center justify-center px-4">
      <div className="bg-white rounded-xl shadow-lg p-8 w-full max-w-md">
        <h1 className="text-2xl font-bold mb-6 text-center">Admin Login</h1>
        <form onSubmit={handleLogin} className="space-y-4">
          <div>
            <label className="block font-semibold mb-2">Password</label>
            <input type="password" value={pw} onChange={e => setPw(e.target.value)} className="w-full border rounded px-4 py-3" required />
            {err && <p className="text-red-500 text-sm mt-2">{err}</p>}
          </div>
          <button type="submit" className="w-full text-white py-3 rounded font-semibold" style={{ background: `linear-gradient(135deg, ${CONFIG.primaryColor}, ${CONFIG.primaryDark})` }}>Login</button>
          <button type="button" onClick={() => navigate('home')} className="w-full border py-3 rounded font-semibold">Kembali</button>
        </form>
      </div>
    </div>
  );
}

function AdminPanel({ campaigns, setCampaigns, donations, setDonations, navigate, setIsAdmin }) {
  const [tab, setTab] = useState('donations');
  
  const approve = (id) => {
    const don = donations.find(d => d.id === id);
    setDonations(prev => prev.map(d => d.id === id ? { ...d, status: 'verified' } : d));
    setCampaigns(prev => prev.map(c => c.id === don.campaignId ? { ...c, collected: c.collected + don.amount, donors: c.donors + 1 } : c));
  };

  return (
    <div className="max-w-7xl mx-auto px-4 py-12">
      <div className="flex justify-between mb-8">
        <h1 className="text-3xl font-bold">Admin Dashboard</h1>
        <button onClick={() => { setIsAdmin(false); navigate('home'); }}><LogOut /></button>
      </div>

      <div className="bg-white rounded-lg shadow">
        <div className="border-b flex">
          <button onClick={() => setTab('donations')} className={`px-6 py-4 font-semibold ${tab === 'donations' ? 'border-b-2' : ''}`} style={{ borderColor: tab === 'donations' ? CONFIG.primaryColor : 'transparent' }}>
            Donasi ({donations.filter(d => d.status === 'pending').length} Pending)
          </button>
          <button onClick={() => setTab('campaigns')} className={`px-6 py-4 font-semibold ${tab === 'campaigns' ? 'border-b-2' : ''}`} style={{ borderColor: tab === 'campaigns' ? CONFIG.primaryColor : 'transparent' }}>
            Campaigns
          </button>
        </div>

        <div className="p-6">
          {tab === 'donations' && (
            <div className="space-y-4">
              {donations.filter(d => d.status === 'pending').map(d => (
                <div key={d.id} className="border rounded p-4">
                  <div className="flex justify-between mb-3">
                    <div>
                      <p className="font-semibold">{d.id}</p>
                      <p>{d.name}</p>
                    </div>
                    <p className="font-bold" style={{ color: CONFIG.primaryColor }}>Rp {d.amount.toLocaleString()}</p>
                  </div>
                  <div className="flex gap-2">
                    <button onClick={() => approve(d.id)} className="flex-1 bg-green-600 text-white py-2 rounded">✓ Approve</button>
                    <button className="px-4 bg-red-600 text-white py-2 rounded">✗ Reject</button>
                  </div>
                </div>
              ))}
            </div>
          )}

          {tab === 'campaigns' && (
            <div className="space-y-4">
              {campaigns.map(c => (
                <div key={c.id} className="border rounded p-4">
                  <p className="font-semibold">{c.title}</p>
                  <p className="text-sm">Rp {(c.collected / 1000000).toFixed(1)} Jt / Rp {(c.target / 1000000).toFixed(1)} Jt</p>
                </div>
              ))}
            </div>
          )}
        </div>
      </div>
    </div>
  );
}

function Calculator({ navigate }) {
  const [amount, setAmount] = useState('');
  const nisab = 85000000;
  const zakat = amount >= nisab ? amount * 0.025 : 0;

  return (
    <div className="max-w-3xl mx-auto px-4 py-12">
      <button onClick={() => navigate('home')} className="mb-6" style={{ color: CONFIG.primaryColor }}>← Kembali</button>
      <div className="bg-white rounded-xl shadow-lg p-8">
        <h1 className="text-3xl font-bold mb-8">Kalkulator Zakat</h1>
        <div className="mb-6">
          <label className="block font-semibold mb-2">Jumlah Harta (Rp)</label>
          <input type="number" value={amount} onChange={e => setAmount(e.target.value)} className="w-full border rounded px-4 py-3" />
        </div>
        {amount && (
          <div className="p-6 rounded border-2" style={{ backgroundColor: `${CONFIG.primaryColor}10`, borderColor: CONFIG.primaryColor }}>
            <p className="mb-2">Nisab: Rp {nisab.toLocaleString()}</p>
            {amount >= nisab ? (
              <div>
                <p className="text-3xl font-bold mb-4" style={{ color: CONFIG.primaryColor }}>Rp {zakat.toLocaleString()}</p>
                <p className="mb-4">✓ Harta mencapai nisab</p>
                <button onClick={() => navigate('home')} className="w-full text-white py-3 rounded font-semibold" style={{ background: `linear-gradient(135deg, ${CONFIG.primaryColor}, ${CONFIG.primaryDark})` }}>
                  Bayar Zakat
                </button>
              </div>
            ) : (
              <p className="text-amber-800">Belum mencapai nisab</p>
            )}
          </div>
        )}
      </div>
    </div>
  );
}

function About({ navigate }) {
  return (
    <div className="max-w-4xl mx-auto px-4 py-12">
      <h1 className="text-4xl font-bold mb-8 text-center">Tentang {CONFIG.platformName}</h1>
      <div className="bg-white rounded-xl shadow-lg p-8 mb-8">
        <p className="text-center mb-6" style={{ color: CONFIG.primaryColor }}>بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيم</p>
        <p className="text-gray-700 mb-4">{CONFIG.platformName} adalah platform donasi Islami yang memudahkan umat untuk menyalurkan zakat, wakaf, infaq, dan qurban dengan amanah dan transparan.</p>
      </div>
      <div className="bg-white rounded-xl shadow-lg p-8">
        <h2 className="text-2xl font-bold mb-4">Hubungi Kami</h2>
        <p className="mb-2"><strong>WhatsApp:</strong> {CONFIG.whatsapp}</p>
        <p className="mb-2"><strong>Email:</strong> {CONFIG.email}</p>
        <p><strong>Instagram:</strong> {CONFIG.instagram}</p>
      </div>
    </div>
  );
}

function Footer() {
  return (
    <footer className="text-white mt-20" style={{ background: `linear-gradient(to bottom, ${CONFIG.primaryDark}, #2d3e15)` }}>
      <div className="max-w-7xl mx-auto px-4 py-12">
        <div className="grid md:grid-cols-4 gap-8">
          <div>
            <div className="flex items-center gap-2 mb-4">
              <Heart size={20} fill="white" />
              <span className="font-bold">{CONFIG.platformName}</span>
            </div>
            <p className="text-green-200 text-sm">Platform Donasi Islami</p>
          </div>
          <div>
            <h3 className="font-bold mb-4">Kategori</h3>
            <div className="space-y-2 text-sm text-green-200">
              <p>Zakat</p>
              <p>Wakaf</p>
              <p>Infaq</p>
              <p>Qurban</p>
            </div>
          </div>
          <div>
            <h3 className="font-bold mb-4">Kontak</h3>
            <p className="text-sm text-green-200">WA: {CONFIG.whatsapp}</p>
            <p className="text-sm text-green-200">{CONFIG.email}</p>
          </div>
          <div>
            <h3 className="font-bold mb-4">Sosial</h3>
            <p className="text-sm text-green-200">{CONFIG.instagram}</p>
          </div>
        </div>
        <div className="border-t border-green-800 mt-8 pt-8 text-center text-green-300 text-sm">
          <p>© 2025 {CONFIG.platformName}. Barakallahu fiikum.</p>
        </div>
      </div>
    </footer>
  );
}

function CampaignCard({ campaign, onClick }) {
  const pct = (campaign.collected / campaign.target) * 100;
  
  return (
    <div onClick={onClick} className="bg-white rounded-xl shadow overflow-hidden cursor-pointer hover:shadow-lg transition">
      <div className="bg-gray-200 h-48 flex items-center justify-center">
        <p className="text-gray-500 text-sm">[Foto]</p>
      </div>
      <div className="p-4">
        <span className="px-3 py-1 rounded-full text-xs font-semibold" style={{ backgroundColor: `${CONFIG.primaryColor}20`, color: CONFIG.primaryColor }}>
          {campaign.category.toUpperCase()}
        </span>
        <h3 className="font-bold mt-2 mb-3 line-clamp-2">{campaign.title}</h3>
        <div className="mb-3">
          <div className="w-full bg-gray-200 rounded-full h-2 mb-2">
            <div className="h-2 rounded-full" style={{ width: `${Math.min(pct, 100)}%`, background: `linear-gradient(90deg, ${CONFIG.primaryColor}, ${CONFIG.primaryDark})` }}></div>
          </div>
          <div className="flex justify-between text-sm">
            <span className="font-semibold" style={{ color: CONFIG.primaryColor }}>Rp {(campaign.collected / 1000000).toFixed(1)} Jt</span>
            <span className="text-gray-600">{pct.toFixed(0)}%</span>
          </div>
        </div>
        <p className="text-sm text-gray-600">{campaign.donors} donatur</p>
      </div>
    </div>
  );
}