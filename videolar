import data from "@/data/videolar.json";

export const metadata = { title: "Videolar — Tarih Atlası" };

export default function Page(){
  return (
    <div className="space-y-8">
      <header className="card">
        <h1 className="text-3xl font-bold">Videolar</h1>
        <p className="text-neutral-300 mt-2">YouTube'daki içeriklerin arşivi.</p>
      </header>
      <div className="grid md:grid-cols-2 gap-6">
        {data.map(v => (
          <article key={v.slug} id={v.slug} className="space-y-2 card">
            <h3 className="text-lg font-semibold">{v.title}</h3>
            <p className="text-neutral-300">{v.summary}</p>
            <div className="aspect-video w-full rounded-xl overflow-hidden">
              <iframe
                className="w-full h-full"
                src={`https://www.youtube.com/embed/${v.youtubeId}`}
                title={v.title}
                frameBorder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                allowFullScreen
              ></iframe>
            </div>
          </article>
        ))}
      </div>
    </div>
  );
}
